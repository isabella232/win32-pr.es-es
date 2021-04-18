---
description: DirectXMath proporciona una solución matemática optimizada para Windows.
ms.assetid: c2a64435-b2fb-3638-2eea-3ed52f4c7cd5
title: Guía de programación de DirectXMath
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df406787776f9fa5d1786e6ed6c5998e27a1c059
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687178"
---
# <a name="directxmath-programming-guide"></a><span data-ttu-id="bf561-103">Guía de programación de DirectXMath</span><span class="sxs-lookup"><span data-stu-id="bf561-103">DirectXMath programming guide</span></span>

<span data-ttu-id="bf561-104">DirectXMath proporciona una solución matemática optimizada para Windows.</span><span class="sxs-lookup"><span data-stu-id="bf561-104">DirectXMath provides a math solution optimized for Windows.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="bf561-105">En esta sección</span><span class="sxs-lookup"><span data-stu-id="bf561-105">In this section</span></span>



| <span data-ttu-id="bf561-106">Tema</span><span class="sxs-lookup"><span data-stu-id="bf561-106">Topic</span></span>                                                             | <span data-ttu-id="bf561-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="bf561-107">Description</span></span>                                                                                                                                                                                                                                                             |
|-------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bf561-108">Introducción</span><span class="sxs-lookup"><span data-stu-id="bf561-108">Getting Started</span></span>](pg-xnamath-getting-started.md)<br/>      | <span data-ttu-id="bf561-109">La biblioteca de DirectXMath implementa una interfaz óptima y portable para operaciones de álgebra aritmética y lineal en vectores de punto flotante de precisión sencilla (2D, 3D y 4D) o matrices (3 × 3 y 4 × 4).</span><span class="sxs-lookup"><span data-stu-id="bf561-109">The DirectXMath Library implements an optimal and portable interface for arithmetic and linear algebra operations on single-precision floating-point vectors (2D, 3D, and 4D) or matrices (3×3 and 4×4).</span></span> <br/>                                                    |
| [<span data-ttu-id="bf561-110">Novedades</span><span class="sxs-lookup"><span data-stu-id="bf561-110">What's New</span></span>](pg-xnamath-whatsnew.md)<br/>                  | <span data-ttu-id="bf561-111">La biblioteca de DirectXMath se basa en la [versión 2,04 de la biblioteca SIMD de C++ matemática de XNA](https://walbourn.github.io/).</span><span class="sxs-lookup"><span data-stu-id="bf561-111">The DirectXMath library is based on the [XNA Math C++ SIMD library version 2.04](https://walbourn.github.io/).</span></span> <span data-ttu-id="bf561-112">Aquí se describe el modo en que DirectXMath difiere de la matemáticas de XNA y cómo difieren las versiones de DirectXMath.</span><span class="sxs-lookup"><span data-stu-id="bf561-112">Here we describe how DirectXMath differs from XNA Math and how DirectXMath versions differ.</span></span> <br/> |
| [<span data-ttu-id="bf561-113">Migración de código</span><span class="sxs-lookup"><span data-stu-id="bf561-113">Code Migration</span></span>](pg-xnamath-migration.md)<br/>             | <span data-ttu-id="bf561-114">En esta información general se describen los cambios necesarios para migrar el código existente mediante la biblioteca matemática de XNA a la biblioteca de DirectXMath.</span><span class="sxs-lookup"><span data-stu-id="bf561-114">This overview describes the changes required to migrate existing code using the XNA Math library to the DirectXMath library.</span></span><br/>                                                                                                                                 |
| [<span data-ttu-id="bf561-115">Trabajo con D3DXMath</span><span class="sxs-lookup"><span data-stu-id="bf561-115">Working with D3DXMath</span></span>](pg-xnamath-migration-d3dx.md)<br/> | <span data-ttu-id="bf561-116">D3DXMath es una biblioteca auxiliar matemática para aplicaciones Direct3D.</span><span class="sxs-lookup"><span data-stu-id="bf561-116">D3DXMath is a math helper library for Direct3D applications.</span></span> <br/>                                                                                                                                                                                                |
| [<span data-ttu-id="bf561-117">Optimización del código</span><span class="sxs-lookup"><span data-stu-id="bf561-117">Code Optimization</span></span>](pg-xnamath-optimizing.md)<br/>         | <span data-ttu-id="bf561-118">En este tema se describen las consideraciones y las estrategias de optimización con la biblioteca de DirectXMath.</span><span class="sxs-lookup"><span data-stu-id="bf561-118">This topic describes optimization considerations and strategies with the DirectXMath Library.</span></span><br/>                                                                                                                                                                |
| [<span data-ttu-id="bf561-119">Elementos internos de la biblioteca</span><span class="sxs-lookup"><span data-stu-id="bf561-119">Library Internals</span></span>](pg-xnamath-internals.md)<br/>          | <span data-ttu-id="bf561-120">En este tema se describe el diseño interno de la biblioteca de DirectXMath.</span><span class="sxs-lookup"><span data-stu-id="bf561-120">This topic describes the internal design of the DirectXMath library.</span></span><br/>                                                                                                                                                                                         |



 

## <a name="related-topics"></a><span data-ttu-id="bf561-121">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="bf561-121">Related Topics</span></span>

<dl> <dt>

<span data-ttu-id="bf561-122"><span id="DirectXMath_Programming_Reference"></span><span id="directxmath_programming_reference"></span><span id="DIRECTXMATH_PROGRAMMING_REFERENCE"></span>[Referencia de programación de DirectXMath](ovw-xnamath-reference.md)</span><span class="sxs-lookup"><span data-stu-id="bf561-122"><span id="DirectXMath_Programming_Reference"></span><span id="directxmath_programming_reference"></span><span id="DIRECTXMATH_PROGRAMMING_REFERENCE"></span>[DirectXMath Programming Reference](ovw-xnamath-reference.md)</span></span>
<span data-ttu-id="bf561-123"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="bf561-123"></dt> <dd></dd> </dl></span></span>

## <a name="related-topics"></a><span data-ttu-id="bf561-124">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="bf561-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bf561-125">DirectXMath</span><span class="sxs-lookup"><span data-stu-id="bf561-125">DirectXMath</span></span>](directxmath-portal.md)
</dt> </dl>

 

 




