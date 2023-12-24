# Event Registration Web Application

## AIM:
To design, develop and deploy a web application for event registration.

## DESIGN STEPS:
## Step 1:
create a new frame.

## Step 2:
select any one present size of your choice

## Step 3:
select the shape you needed.

## Step 4:
Import images as needed and create pages based on your need and link there.

## Step 5:
Validate the HTML and CSS code.

## Step 6:
Publish the website in the given URL.

## DESIGN:
FIGMA

## PROGRAM :
```py
import React from 'react'
<% if (variantSvgs) { %>
const renderSvgs = ({
  activeColor,
  className,
  desc,
  focusColor,
  height,
  hoverColor,
  color,
  title,
  width,
  <% _.each(variants, (variantValues, variantKey) => { %>
  <%= variantKey %>,
  <% }) %>
}) => {
  <% _.each(variantSvgs, (variantSvg, i) => { %>
  <%= (i === 0) ? 'if (' : 'else if (' %><% variantSvg.variants.map((variant, j) => { %><%= variant.key %> === <%= typeof(variant.value) === 'boolean' ? "" : "'" %><%= variant.value %><%= typeof(variant.value) === 'boolean' ? "" : "'" %><%= (j < variantSvg.variants.length - 1) ? ' && ' : '' %><% }) %>) {
    return (
      <svg
        {...{ className }}
        <% if (variantSvg.defaultFill) { %>
        data-hover={hoverColor}
        data-focus={focusColor}
        data-active={activeColor}
        <% } %>
        width={width ? width : height ? undefined : <%= variantSvg.attributes.width ? '"' + variantSvg.attributes.width + '"' : 'undefined' %>}
        height={height ? height : undefined}
        <% if (variantSvg.attributes.viewBox) { %>viewBox="<%= variantSvg.attributes.viewBox %>" <% } %>
        <% if (variantSvg.defaultFill) { %>
        fill={color || "<%= variantSvg.defaultFill %>"}
        <% } else { %>
        <% if (variantSvg.attributes.fill) { %>fill="<%= variantSvg.attributes.fill %>"<% } %>
        <% } %>
        xmlns="<%= variantSvg.attributes.xmlns ? variantSvg.attributes.xmlns : 'http://www.w3.org/2000/svg'%>"
        <%= variantSvg.attributes.other %>
      >
        {!!title && <title>{title}</title>}
        {!!desc && <desc>{desc}</desc>}

        <%= variantSvg.contents %>
      </svg>
    )
  }
  <% }) %>
  else {
    return (
      <svg
        {...{ className }}
        <% if (svg.defaultFill) { %>
        data-hover={hoverColor}
        data-focus={focusColor}
        data-active={activeColor}
        <% } %>
        width={width ? width : height ? undefined : <%= svg.attributes.width ? '"' + svg.attributes.width + '"' : 'undefined' %>}
        height={height ? height : undefined}
        <% if (svg.attributes.viewBox) { %>viewBox="<%= svg.attributes.viewBox %>" <% } %>
        <% if (svg.defaultFill) { %>
        fill={color || "<%= svg.defaultFill %>"}
        <% } else { %>
        <% if (svg.attributes.fill) { %>fill="<%= svg.attributes.fill %>"<% } %>
        <% } %>
        xmlns="<%= svg.attributes.xmlns ? svg.attributes.xmlns : 'http://www.w3.org/2000/svg' %>"
        <%= svg.attributes.other %>
      >
        {!!title && <title>{title}</title>}
        {!!desc && <desc>{desc}</desc>}

        <%= svg.contents %>
      </svg>
    )
  }
}
<% } %>
const <%= name %> = ({
  <% if (svg.defaultFill || variantSvgs) { %>activeColor,<% } %>
  className,
  <% if (svg.defaultFill || variantSvgs) { %>color,<% } %>
  desc,
  <% if (svg.defaultFill || variantSvgs) { %>focusColor,<% } %>
  height,
  <% if (svg.defaultFill || variantSvgs) { %>hoverColor,<% } %>
  title,
  width,
  <% _.each(variants, (variantValues, variantKey) => { %>
  <%= variantKey %>,
  <% }) %>
}) => {
  <% if (svg.defaultFill || variantSvgs) { %>
  const css = `
    ${hoverColor ? `svg[data-hover="${hoverColor}"]:hover {
      fill: ${hoverColor};
    }` : ''}
    ${focusColor ? `svg[data-focus="${focusColor}"]:focus {
      fill: ${focusColor};
    }` : ''}
    ${activeColor ? `svg[data-active="${activeColor}"]:active {
      fill: ${activeColor};
    }` : ''}
  `
  <% } %>

  return (
    <% if (svg.defaultFill || variantSvgs) { %><React.Fragment><% } %>
      <% if (svg.defaultFill || variantSvgs) { %>
      <style>
        {css}
      </style>
      <% } %>

      <% if (variantSvgs) { %>
      {renderSvgs({
        activeColor,
        className,
        desc,
        focusColor,
        height,
        hoverColor,
        color,
        title,
        width,
        <% _.each(variants, (variantValues, variantKey) => { %>
        <%= variantKey %>,
        <% }) %>
      })}
      <% } else { %>
      <svg
        {...{ className }}
        <% if (svg.defaultFill) { %>
        data-hover={hoverColor}
        data-focus={focusColor}
        data-active={activeColor}
        <% } %>
        width={width ? width : height ? undefined : <%= svg.attributes.width ? '"' + svg.attributes.width + '"' : 'undefined' %>}
        height={height ? height : undefined}
        <% if (svg.attributes.viewBox) { %>viewBox="<%= svg.attributes.viewBox %>" <% } %>
        <% if (svg.defaultFill) { %>
        fill={color || "<%= svg.defaultFill %>"}
        <% } else { %>
        <% if (svg.attributes.fill) { %>fill="<%= svg.attributes.fill %>"<% } %>
        <% } %>
        xmlns="<%= svg.attributes.xmlns ? svg.attributes.xmlns : 'http://www.w3.org/2000/svg' %>"
        <%= svg.attributes.other %>
      >
        {!!title && <title>{title}</title>}
        {!!desc && <desc>{desc}</desc>}

        <%= svg.contents %>
      </svg>
      <% } %>
    <% if (svg.defaultFill || variantSvgs) { %></React.Fragment><% } %>
  )
}

export default <%= name %>
```

## OUTPUT:
![](./Desktop%20-%201.png)
![](./Desktop%20-%202.png)
![](./Desktop%20-%203.png)
## Result:
The program to design .develope and display a web application for event registration is completed successfully.