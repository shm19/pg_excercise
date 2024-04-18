--
-- PostgreSQL database dump
--

-- Dumped from database version 12.17 (Ubuntu 12.17-1.pgdg22.04+1)
-- Dumped by pg_dump version 12.17 (Ubuntu 12.17-1.pgdg22.04+1)

SET statement_timeout = 0;
SET lock_timeout = 0;
SET idle_in_transaction_session_timeout = 0;
SET client_encoding = 'UTF8';
SET standard_conforming_strings = on;
SELECT pg_catalog.set_config('search_path', '', false);
SET check_function_bodies = false;
SET xmloption = content;
SET client_min_messages = warning;
SET row_security = off;

DROP DATABASE universe;
--
-- Name: universe; Type: DATABASE; Schema: -; Owner: freecodecamp
--

CREATE DATABASE universe WITH TEMPLATE = template0 ENCODING = 'UTF8' LC_COLLATE = 'C.UTF-8' LC_CTYPE = 'C.UTF-8';


ALTER DATABASE universe OWNER TO freecodecamp;

\connect universe

SET statement_timeout = 0;
SET lock_timeout = 0;
SET idle_in_transaction_session_timeout = 0;
SET client_encoding = 'UTF8';
SET standard_conforming_strings = on;
SELECT pg_catalog.set_config('search_path', '', false);
SET check_function_bodies = false;
SET xmloption = content;
SET client_min_messages = warning;
SET row_security = off;

SET default_tablespace = '';

SET default_table_access_method = heap;

--
-- Name: astronomical_body_feature; Type: TABLE; Schema: public; Owner: freecodecamp
--

CREATE TABLE public.astronomical_body_feature (
    astronomical_body_feature_id integer NOT NULL,
    name character varying(50) NOT NULL,
    body_id integer NOT NULL,
    body_type character varying(50) NOT NULL,
    feature_name character varying(100) NOT NULL,
    description text
);


ALTER TABLE public.astronomical_body_feature OWNER TO freecodecamp;

--
-- Name: astronomical_body_feature_astronomical_body_feature_id_seq; Type: SEQUENCE; Schema: public; Owner: freecodecamp
--

CREATE SEQUENCE public.astronomical_body_feature_astronomical_body_feature_id_seq
    AS integer
    START WITH 1
    INCREMENT BY 1
    NO MINVALUE
    NO MAXVALUE
    CACHE 1;


ALTER TABLE public.astronomical_body_feature_astronomical_body_feature_id_seq OWNER TO freecodecamp;

--
-- Name: astronomical_body_feature_astronomical_body_feature_id_seq; Type: SEQUENCE OWNED BY; Schema: public; Owner: freecodecamp
--

ALTER SEQUENCE public.astronomical_body_feature_astronomical_body_feature_id_seq OWNED BY public.astronomical_body_feature.astronomical_body_feature_id;


--
-- Name: galaxy; Type: TABLE; Schema: public; Owner: freecodecamp
--

CREATE TABLE public.galaxy (
    galaxy_id integer NOT NULL,
    name character varying(50) NOT NULL,
    size_in_miles double precision NOT NULL,
    type character varying(50) NOT NULL,
    discovered_by character varying(100)
);


ALTER TABLE public.galaxy OWNER TO freecodecamp;

--
-- Name: galaxy_galaxy_id_seq; Type: SEQUENCE; Schema: public; Owner: freecodecamp
--

CREATE SEQUENCE public.galaxy_galaxy_id_seq
    AS integer
    START WITH 1
    INCREMENT BY 1
    NO MINVALUE
    NO MAXVALUE
    CACHE 1;


ALTER TABLE public.galaxy_galaxy_id_seq OWNER TO freecodecamp;

--
-- Name: galaxy_galaxy_id_seq; Type: SEQUENCE OWNED BY; Schema: public; Owner: freecodecamp
--

ALTER SEQUENCE public.galaxy_galaxy_id_seq OWNED BY public.galaxy.galaxy_id;


--
-- Name: moon; Type: TABLE; Schema: public; Owner: freecodecamp
--

CREATE TABLE public.moon (
    moon_id integer NOT NULL,
    name character varying(50) NOT NULL,
    planet_id integer NOT NULL,
    surface_area_km2 double precision,
    has_life boolean
);


ALTER TABLE public.moon OWNER TO freecodecamp;

--
-- Name: moon_moon_id_seq; Type: SEQUENCE; Schema: public; Owner: freecodecamp
--

CREATE SEQUENCE public.moon_moon_id_seq
    AS integer
    START WITH 1
    INCREMENT BY 1
    NO MINVALUE
    NO MAXVALUE
    CACHE 1;


ALTER TABLE public.moon_moon_id_seq OWNER TO freecodecamp;

--
-- Name: moon_moon_id_seq; Type: SEQUENCE OWNED BY; Schema: public; Owner: freecodecamp
--

ALTER SEQUENCE public.moon_moon_id_seq OWNED BY public.moon.moon_id;


--
-- Name: planet; Type: TABLE; Schema: public; Owner: freecodecamp
--

CREATE TABLE public.planet (
    planet_id integer NOT NULL,
    name character varying(50) NOT NULL,
    type character varying(50) NOT NULL,
    has_atmosphere boolean,
    population integer,
    radious integer,
    star_id integer NOT NULL
);


ALTER TABLE public.planet OWNER TO freecodecamp;

--
-- Name: planet_planet_id_seq; Type: SEQUENCE; Schema: public; Owner: freecodecamp
--

CREATE SEQUENCE public.planet_planet_id_seq
    AS integer
    START WITH 1
    INCREMENT BY 1
    NO MINVALUE
    NO MAXVALUE
    CACHE 1;


ALTER TABLE public.planet_planet_id_seq OWNER TO freecodecamp;

--
-- Name: planet_planet_id_seq; Type: SEQUENCE OWNED BY; Schema: public; Owner: freecodecamp
--

ALTER SEQUENCE public.planet_planet_id_seq OWNED BY public.planet.planet_id;


--
-- Name: star; Type: TABLE; Schema: public; Owner: freecodecamp
--

CREATE TABLE public.star (
    star_id integer NOT NULL,
    name character varying(50) NOT NULL,
    type character varying(50) NOT NULL,
    galaxy_id integer NOT NULL,
    temperature_k numeric,
    is_visible_from_earth boolean
);


ALTER TABLE public.star OWNER TO freecodecamp;

--
-- Name: star_star_id_seq; Type: SEQUENCE; Schema: public; Owner: freecodecamp
--

CREATE SEQUENCE public.star_star_id_seq
    AS integer
    START WITH 1
    INCREMENT BY 1
    NO MINVALUE
    NO MAXVALUE
    CACHE 1;


ALTER TABLE public.star_star_id_seq OWNER TO freecodecamp;

--
-- Name: star_star_id_seq; Type: SEQUENCE OWNED BY; Schema: public; Owner: freecodecamp
--

ALTER SEQUENCE public.star_star_id_seq OWNED BY public.star.star_id;


--
-- Name: astronomical_body_feature astronomical_body_feature_id; Type: DEFAULT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.astronomical_body_feature ALTER COLUMN astronomical_body_feature_id SET DEFAULT nextval('public.astronomical_body_feature_astronomical_body_feature_id_seq'::regclass);


--
-- Name: galaxy galaxy_id; Type: DEFAULT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.galaxy ALTER COLUMN galaxy_id SET DEFAULT nextval('public.galaxy_galaxy_id_seq'::regclass);


--
-- Name: moon moon_id; Type: DEFAULT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.moon ALTER COLUMN moon_id SET DEFAULT nextval('public.moon_moon_id_seq'::regclass);


--
-- Name: planet planet_id; Type: DEFAULT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.planet ALTER COLUMN planet_id SET DEFAULT nextval('public.planet_planet_id_seq'::regclass);


--
-- Name: star star_id; Type: DEFAULT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.star ALTER COLUMN star_id SET DEFAULT nextval('public.star_star_id_seq'::regclass);


--
-- Data for Name: astronomical_body_feature; Type: TABLE DATA; Schema: public; Owner: freecodecamp
--

INSERT INTO public.astronomical_body_feature VALUES (1, 'name 1', 1, 'planet', 'Oceans', 'Earth is the only planet in our solar system known to have large bodies of liquid water.');
INSERT INTO public.astronomical_body_feature VALUES (2, 'name 2', 4, 'planet', 'Great Red Spot', 'A gigantic storm located on Jupiter, visible for over 350 years.');
INSERT INTO public.astronomical_body_feature VALUES (3, 'name 3', 2, 'moon', 'Ice Crust', 'Phobos has a smooth surface of ice and rock.');
INSERT INTO public.astronomical_body_feature VALUES (4, 'name 4', 1, 'galaxy', 'Milky Way Bar', 'Our galaxy has a prominent bar-shaped core of stars.');
INSERT INTO public.astronomical_body_feature VALUES (5, 'name 5', 1, 'star', 'Solar Flares', 'The Sun exhibits massive solar flares that extend into space.');


--
-- Data for Name: galaxy; Type: TABLE DATA; Schema: public; Owner: freecodecamp
--

INSERT INTO public.galaxy VALUES (1, 'Milky Way', 58786000000, 'Spiral', 'Galileo Galilei');
INSERT INTO public.galaxy VALUES (2, 'Andromeda', 72000000000, 'Spiral', 'Simon Marius');
INSERT INTO public.galaxy VALUES (3, 'Triangulum', 50000000000, 'Spiral', 'Edward Pigott');
INSERT INTO public.galaxy VALUES (4, 'Whirlpool', 60000000000, 'Spiral', 'Charles Messier');
INSERT INTO public.galaxy VALUES (5, 'Sombrero', 30000000000, 'Elliptical', 'Pierre Méchain');
INSERT INTO public.galaxy VALUES (6, 'Pinwheel', 52000000000, 'Spiral', 'William Herschel');


--
-- Data for Name: moon; Type: TABLE DATA; Schema: public; Owner: freecodecamp
--

INSERT INTO public.moon VALUES (21, 'Moon', 1, 37932000, false);
INSERT INTO public.moon VALUES (22, 'Deimos', 2, 124, false);
INSERT INTO public.moon VALUES (23, 'Phobos', 2, 154, false);
INSERT INTO public.moon VALUES (24, 'Io', 4, 3620000, false);
INSERT INTO public.moon VALUES (25, 'Europa', 4, 3080000, false);
INSERT INTO public.moon VALUES (26, 'Ganymede', 4, 8680000, false);
INSERT INTO public.moon VALUES (27, 'Callisto', 4, 7300000, false);
INSERT INTO public.moon VALUES (28, 'Titan', 5, 8320000, false);
INSERT INTO public.moon VALUES (29, 'Rhea', 5, 1520000, false);
INSERT INTO public.moon VALUES (30, 'Iapetus', 5, 1469000, false);
INSERT INTO public.moon VALUES (31, 'Oberon', 6, 7614000, false);
INSERT INTO public.moon VALUES (32, 'Miranda', 6, 235600, false);
INSERT INTO public.moon VALUES (33, 'Triton', 7, 2300000, false);
INSERT INTO public.moon VALUES (34, 'Proteus', 7, 430000, false);
INSERT INTO public.moon VALUES (35, 'Charon', 8, 1750000, false);
INSERT INTO public.moon VALUES (36, 'Nix', 8, 700, false);
INSERT INTO public.moon VALUES (37, 'Hydra', 8, 500, false);
INSERT INTO public.moon VALUES (38, 'Styx', 8, 350, false);
INSERT INTO public.moon VALUES (39, 'Kerberos', 8, 310, false);
INSERT INTO public.moon VALUES (40, 'Namaka', 9, 1700, false);


--
-- Data for Name: planet; Type: TABLE DATA; Schema: public; Owner: freecodecamp
--

INSERT INTO public.planet VALUES (1, 'Earth', 'Terrestrial', true, 78000, NULL, 1);
INSERT INTO public.planet VALUES (2, 'Mars', 'Terrestrial', true, 0, NULL, 1);
INSERT INTO public.planet VALUES (3, 'Venus', 'Terrestrial', true, 0, NULL, 1);
INSERT INTO public.planet VALUES (4, 'Jupiter', 'Gas Giant', true, 0, NULL, 1);
INSERT INTO public.planet VALUES (5, 'Saturn', 'Gas Giant', true, 0, NULL, 1);
INSERT INTO public.planet VALUES (6, 'Neptune', 'Ice Giant', true, 0, NULL, 1);
INSERT INTO public.planet VALUES (7, 'Uranus', 'Ice Giant', true, 0, NULL, 1);
INSERT INTO public.planet VALUES (8, 'Pluto', 'Dwarf', false, 0, NULL, 1);
INSERT INTO public.planet VALUES (9, 'Mercury', 'Terrestrial', false, 0, NULL, 1);
INSERT INTO public.planet VALUES (10, 'Kepler-22b', 'Exoplanet', true, 0, NULL, 2);
INSERT INTO public.planet VALUES (11, 'Proxima b', 'Exoplanet', true, 0, NULL, 3);
INSERT INTO public.planet VALUES (12, 'Gliese 581d', 'Exoplanet', true, 0, NULL, 4);


--
-- Data for Name: star; Type: TABLE DATA; Schema: public; Owner: freecodecamp
--

INSERT INTO public.star VALUES (1, 'Sun', 'G-Type', 1, 5778, true);
INSERT INTO public.star VALUES (2, 'Sirius', 'A-Type', 1, 9940, true);
INSERT INTO public.star VALUES (3, 'Alpha Centauri', 'G-Type', 1, 5790, true);
INSERT INTO public.star VALUES (4, 'Betelgeuse', 'M-Type', 1, 3500, false);
INSERT INTO public.star VALUES (5, 'Vega', 'A-Type', 1, 9602, true);
INSERT INTO public.star VALUES (6, 'Rigel', 'B-Type', 1, 12100, false);


--
-- Name: astronomical_body_feature_astronomical_body_feature_id_seq; Type: SEQUENCE SET; Schema: public; Owner: freecodecamp
--

SELECT pg_catalog.setval('public.astronomical_body_feature_astronomical_body_feature_id_seq', 6, true);


--
-- Name: galaxy_galaxy_id_seq; Type: SEQUENCE SET; Schema: public; Owner: freecodecamp
--

SELECT pg_catalog.setval('public.galaxy_galaxy_id_seq', 7, true);


--
-- Name: moon_moon_id_seq; Type: SEQUENCE SET; Schema: public; Owner: freecodecamp
--

SELECT pg_catalog.setval('public.moon_moon_id_seq', 40, true);


--
-- Name: planet_planet_id_seq; Type: SEQUENCE SET; Schema: public; Owner: freecodecamp
--

SELECT pg_catalog.setval('public.planet_planet_id_seq', 13, true);


--
-- Name: star_star_id_seq; Type: SEQUENCE SET; Schema: public; Owner: freecodecamp
--

SELECT pg_catalog.setval('public.star_star_id_seq', 7, true);


--
-- Name: astronomical_body_feature astronomical_body_feature_name_key; Type: CONSTRAINT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.astronomical_body_feature
    ADD CONSTRAINT astronomical_body_feature_name_key UNIQUE (name);


--
-- Name: astronomical_body_feature astronomical_body_feature_pkey; Type: CONSTRAINT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.astronomical_body_feature
    ADD CONSTRAINT astronomical_body_feature_pkey PRIMARY KEY (astronomical_body_feature_id);


--
-- Name: galaxy galaxy_name_key; Type: CONSTRAINT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.galaxy
    ADD CONSTRAINT galaxy_name_key UNIQUE (name);


--
-- Name: galaxy galaxy_pkey; Type: CONSTRAINT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.galaxy
    ADD CONSTRAINT galaxy_pkey PRIMARY KEY (galaxy_id);


--
-- Name: moon moon_name_key; Type: CONSTRAINT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.moon
    ADD CONSTRAINT moon_name_key UNIQUE (name);


--
-- Name: moon moon_pkey; Type: CONSTRAINT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.moon
    ADD CONSTRAINT moon_pkey PRIMARY KEY (moon_id);


--
-- Name: planet planet_name_key; Type: CONSTRAINT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.planet
    ADD CONSTRAINT planet_name_key UNIQUE (name);


--
-- Name: planet planet_pkey; Type: CONSTRAINT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.planet
    ADD CONSTRAINT planet_pkey PRIMARY KEY (planet_id);


--
-- Name: star star_name_key; Type: CONSTRAINT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.star
    ADD CONSTRAINT star_name_key UNIQUE (name);


--
-- Name: star star_pkey; Type: CONSTRAINT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.star
    ADD CONSTRAINT star_pkey PRIMARY KEY (star_id);


--
-- Name: moon moon_planet_id_fkey; Type: FK CONSTRAINT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.moon
    ADD CONSTRAINT moon_planet_id_fkey FOREIGN KEY (planet_id) REFERENCES public.planet(planet_id);


--
-- Name: planet planet_star_id_fkey; Type: FK CONSTRAINT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.planet
    ADD CONSTRAINT planet_star_id_fkey FOREIGN KEY (star_id) REFERENCES public.star(star_id);


--
-- Name: star star_galaxy_id_fkey; Type: FK CONSTRAINT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.star
    ADD CONSTRAINT star_galaxy_id_fkey FOREIGN KEY (galaxy_id) REFERENCES public.galaxy(galaxy_id);


--
-- PostgreSQL database dump complete
--

