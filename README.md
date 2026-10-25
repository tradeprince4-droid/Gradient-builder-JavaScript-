function gradient(angle, stops) {
  const list = stops.map(([c, p]) => `${c} ${p}%`).join(", ");
  return {
    css: `background: linear-gradient(${angle}deg, ${list});`,
    tailwind: `bg-gradient-to-r from-[${stops[0][0]}] to-[${stops.at(-1)[0]}]`,
  };
}

console.log(gradient(135, [["#00F5D4", 0], ["#F15BB5", 100]]));# Gradient-builder-JavaScript-
