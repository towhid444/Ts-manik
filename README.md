// ts-manik-portfolio/src/App.jsx import React from 'react'; import { BrowserRouter as Router, Routes, Route, Link } from 'react-router-dom'; import Home from './pages/Home'; import About from './pages/About'; import Gallery from './pages/Gallery'; import Contact from './pages/Contact'; import './App.css';

export default function App() { return ( <Router> <div className="bg-gray-900 text-white min-h-screen"> <header className="p-4 flex justify-between items-center shadow-md"> <h1 className="text-2xl font-bold">Ts Manik</h1> <nav className="space-x-4"> <Link to="/" className="hover:underline">Home</Link> <Link to="/about" className="hover:underline">About</Link> <Link to="/gallery" className="hover:underline">Gallery</Link> <Link to="/contact" className="hover:underline">Contact</Link> </nav> </header>

<main className="p-4">
      <Routes>
        <Route path="/" element={<Home />} />
        <Route path="/about" element={<About />} />
        <Route path="/gallery" element={<Gallery />} />
        <Route path="/contact" element={<Contact />} />
      </Routes>
    </main>
  </div>
</Router>

); }


