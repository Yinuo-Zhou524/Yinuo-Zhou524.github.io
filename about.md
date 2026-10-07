---
layout: default
title: About
---

# About Me

## Background

I grew up and began my forestry training in China, then continued my studies in New Brunswick, Canada, where I became deeply interested in tree mortality, dendrochronology, and forest health. 

## Current Status

I am a Ph.D. candidate in the School of Renewable Natural Resources at Louisiana State University. I work in Dr. Brett Wolfe’s lab.

<div class="photo-grid photo-grid-compact">
  <figure class="photo-figure">
    <a href="{{ '/assets/img/lab1.jpg' | relative_url }}" target="_blank">
      <img src="{{ '/assets/img/lab1.jpg' | relative_url }}" alt="In Dr. Brett Wolfe's lab" class="grid-photo">
    </a>
  </figure>
  <figure class="photo-figure">
    <a href="{{ '/assets/img/lab2.jpg' | relative_url }}" target="_blank">
      <img src="{{ '/assets/img/lab3.jpg' | relative_url }}" alt="Lab work and measurements" class="grid-photo">
    </a>
  </figure>
</div>

My research examines how bark and other non-foliar tissues contribute to plant water relations and stress responses.

I am particularly interested in bark water vapor conductance, lenticel function, flooding responses, and the role of residual water loss in tree physiology and mortality. My work combines field ecology, controlled experiments, anatomical measurements, and quantitative analysis.

My current favorite tree species is bald cypress (*Taxodium distichum*). In Chinese, bald cypress is called “落羽杉”, which means “falling feathers.”

Outside of research, I love racket sports (tennis, table tennis, and pickleball). I spend much of my leisure time reading, doing yoga, and fostering neonatal kittens.

## A Few Things I Enjoy Outside of Research

<div class="photo-grid photo-grid-compact">
  <figure class="photo-figure">
    <a href="{{ '/assets/img/hobby_yoga.jpg' | relative_url }}" target="_blank">
      <img src="{{ '/assets/img/hobby_yoga.jpg' | relative_url }}" alt="Doing yoga" class="grid-photo">
    </a>
    <figcaption>Bird in the house</figcaption>
  </figure>

  <figure class="photo-figure">
    <a href="{{ '/assets/img/foster.jpg' | relative_url }}" target="_blank">
      <img src="{{ '/assets/img/foster.jpg' | relative_url }}" alt="Fostering neonatal kittens" class="grid-photo">
    </a>
    <figcaption>Fostering neonate kittens</figcaption>
  </figure>

  <figure class="photo-figure">
    <a href="{{ '/assets/img/tt.jpg' | relative_url }}" target="_blank">
      <img src="{{ '/assets/img/tt.jpg' | relative_url }}" alt="Playing table tennis" class="grid-photo">
    </a>
    <figcaption>NCTTA</figcaption>
  </figure>
</div>
<div class="cloudy-card">
  <div class="cloudy-photo-wrap">
    <img
      src="{{ '/assets/img/cloudy.JPEG' | relative_url }}"
      alt="Cloudy the cat"
      class="cloudy-photo"
    >

    <div id="heart-container" class="heart-container"></div>
  </div>

  <div class="cloudy-content">
    <p>
      Cloudy is my professional napper, research supervisor, and occasional keyboard assistant.
    </p>

    <button id="pet-cloudy" class="pet-button" type="button">
      ♡ Pet me
    </button>

    <p id="pet-count" class="pet-count"></p>
  </div>
</div>
<script>
  let pets = Number(localStorage.getItem("cloudyPets")) || 0;

  const petButton = document.getElementById("pet-cloudy");
  const petCount = document.getElementById("pet-count");
  const heartContainer = document.getElementById("heart-container");

  function updatePetCount() {
    petCount.textContent =
      pets === 0
        ? "Cloudy is waiting for pets."
        : `You have given Cloudy ${pets} ${pets === 1 ? "pet" : "pets"}.`;
  }

  function makeHeart() {
    const heart = document.createElement("span");
    heart.className = "floating-heart";
    heart.textContent = "♥";

    const randomOffset = Math.random() * 80 - 40;
    heart.style.marginLeft = `${randomOffset}px`;

    heartContainer.appendChild(heart);

    setTimeout(() => heart.remove(), 1100);
  }

  updatePetCount();

  petButton.addEventListener("click", function () {
    pets++;
    localStorage.setItem("cloudyPets", pets);

    petButton.textContent = "♥ Petted!";
    updatePetCount();
    makeHeart();

    setTimeout(() => {
      petButton.textContent = "♡ Pet me";
    }, 600);
  });
</script>