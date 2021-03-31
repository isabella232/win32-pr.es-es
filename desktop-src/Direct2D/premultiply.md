---
title: Premultiplicar efecto
description: Utilice este efecto para convertir una imagen de unpremultiplied Alpha en alfa premultiplicado.
ms.assetid: 8A5F55C6-3AC7-48B4-87D8-C19D8B4EA0DD
keywords:
- premultiplicar efecto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a01a8a9ba005ed688a96254856897b3514f05fd5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996708"
---
# <a name="premultiply-effect"></a><span data-ttu-id="d483b-104">Premultiplicar efecto</span><span class="sxs-lookup"><span data-stu-id="d483b-104">Premultiply effect</span></span>

<span data-ttu-id="d483b-105">Utilice este efecto para convertir una imagen de unpremultiplied Alpha en alfa premultiplicado.</span><span class="sxs-lookup"><span data-stu-id="d483b-105">Use this effect to convert an image from unpremultiplied alpha to premultiplied alpha.</span></span> <span data-ttu-id="d483b-106">El efecto reemplaza cada píxel `P = {R, G, B, A}` de entrada por `P' = {R*A, G*A, B*A, A}` en la salida.</span><span class="sxs-lookup"><span data-stu-id="d483b-106">The effect replaces each input pixel `P = {R, G, B, A}` with `P' = {R*A, G*A, B*A, A}` in the output.</span></span>

<span data-ttu-id="d483b-107">Este efecto no tiene propiedades.</span><span class="sxs-lookup"><span data-stu-id="d483b-107">This effect has no properties.</span></span>

<span data-ttu-id="d483b-108">El CLSID para este efecto es CLSID \_ D2D1Premultiply.</span><span class="sxs-lookup"><span data-stu-id="d483b-108">The CLSID for this effect is CLSID\_D2D1Premultiply.</span></span>

## <a name="output-bitmap"></a><span data-ttu-id="d483b-109">Mapa de bits de salida</span><span class="sxs-lookup"><span data-stu-id="d483b-109">Output bitmap</span></span>

<span data-ttu-id="d483b-110">El tamaño del mapa de bits de salida es el mismo que el tamaño del mapa de bits de entrada.</span><span class="sxs-lookup"><span data-stu-id="d483b-110">The output bitmap size is the same as the input bitmap size.</span></span>

## <a name="requirements"></a><span data-ttu-id="d483b-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d483b-111">Requirements</span></span>



| <span data-ttu-id="d483b-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="d483b-112">Requirement</span></span> | <span data-ttu-id="d483b-113">Value</span><span class="sxs-lookup"><span data-stu-id="d483b-113">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d483b-114">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d483b-114">Minimum supported client</span></span> | <span data-ttu-id="d483b-115">Windows 8 y actualización de la plataforma para aplicaciones de escritorio de Windows 7 aplicaciones de la \[ \| tienda Windows\]</span><span class="sxs-lookup"><span data-stu-id="d483b-115">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="d483b-116">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d483b-116">Minimum supported server</span></span> | <span data-ttu-id="d483b-117">Windows 8 y actualización de la plataforma para aplicaciones de escritorio de Windows 7 aplicaciones de la \[ \| tienda Windows\]</span><span class="sxs-lookup"><span data-stu-id="d483b-117">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="d483b-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d483b-118">Header</span></span>                   | <span data-ttu-id="d483b-119">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="d483b-119">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="d483b-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d483b-120">Library</span></span>                  | <span data-ttu-id="d483b-121">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="d483b-121">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="d483b-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d483b-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d483b-123">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="d483b-123">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

 
