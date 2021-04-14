---
title: Efecto Unpremultiply
description: Utilice este efecto para convertir una imagen de alfa premultiplicada a unpremultiplied alfa.
ms.assetid: A4FAF899-81DA-4BDA-98B4-DE63EC1664F5
keywords:
- efecto unpremultiply
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5628ea646443a08abffa4549ad25147deb609acf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422514"
---
# <a name="unpremultiply-effect"></a><span data-ttu-id="524d2-104">Efecto Unpremultiply</span><span class="sxs-lookup"><span data-stu-id="524d2-104">Unpremultiply effect</span></span>

<span data-ttu-id="524d2-105">Utilice este efecto para convertir una imagen de alfa premultiplicada a unpremultiplied alfa.</span><span class="sxs-lookup"><span data-stu-id="524d2-105">Use this effect to convert an image from premultiplied alpha to unpremultiplied alpha.</span></span> <span data-ttu-id="524d2-106">El efecto reemplaza cada píxel `P = {R, G, B, A}` de entrada por `P' = {R/A, G/A, B/A, A}` en la salida.</span><span class="sxs-lookup"><span data-stu-id="524d2-106">The effect replaces each input pixel `P = {R, G, B, A}` with `P' = {R/A, G/A, B/A, A}` in the output.</span></span>

<span data-ttu-id="524d2-107">Este efecto no tiene propiedades.</span><span class="sxs-lookup"><span data-stu-id="524d2-107">This effect has no properties.</span></span>

<span data-ttu-id="524d2-108">El CLSID para este efecto es CLSID \_ D2D1Unpremultiply.</span><span class="sxs-lookup"><span data-stu-id="524d2-108">The CLSID for this effect is CLSID\_D2D1Unpremultiply.</span></span>

## <a name="output-bitmap"></a><span data-ttu-id="524d2-109">Mapa de bits de salida</span><span class="sxs-lookup"><span data-stu-id="524d2-109">Output bitmap</span></span>

<span data-ttu-id="524d2-110">El tamaño del mapa de bits de salida es el mismo que el tamaño del mapa de bits de entrada.</span><span class="sxs-lookup"><span data-stu-id="524d2-110">The output bitmap size is the same as the input bitmap size.</span></span>

## <a name="requirements"></a><span data-ttu-id="524d2-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="524d2-111">Requirements</span></span>



| <span data-ttu-id="524d2-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="524d2-112">Requirement</span></span> | <span data-ttu-id="524d2-113">Value</span><span class="sxs-lookup"><span data-stu-id="524d2-113">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="524d2-114">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="524d2-114">Minimum supported client</span></span> | <span data-ttu-id="524d2-115">Windows 8 y actualización de la plataforma para aplicaciones de escritorio de Windows 7 aplicaciones de la \[ \| tienda Windows\]</span><span class="sxs-lookup"><span data-stu-id="524d2-115">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="524d2-116">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="524d2-116">Minimum supported server</span></span> | <span data-ttu-id="524d2-117">Windows 8 y actualización de la plataforma para aplicaciones de escritorio de Windows 7 aplicaciones de la \[ \| tienda Windows\]</span><span class="sxs-lookup"><span data-stu-id="524d2-117">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="524d2-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="524d2-118">Header</span></span>                   | <span data-ttu-id="524d2-119">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="524d2-119">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="524d2-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="524d2-120">Library</span></span>                  | <span data-ttu-id="524d2-121">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="524d2-121">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="524d2-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="524d2-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="524d2-123">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="524d2-123">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

 
