---
description: Extensiones de la interfaz IPixEngine4 que contienen adiciones para ver las texturas.
MS-HAID: vspixengine.IPixEngine5
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Interfaz IPixEngine5
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 8995B617-6830-4A07-8C83-B5925E033967
api_name:
- IPixEngine5
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 300ed31eae5d8ff4009f28691c5348db7cd89d6e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537191"
---
# <a name="span-idvspixengineipixengine5spanipixengine5-interface"></a><span data-ttu-id="c8d2b-103"><span id="vspixengine.ipixengine5"></span>Interfaz IPixEngine5</span><span class="sxs-lookup"><span data-stu-id="c8d2b-103"><span id="vspixengine.ipixengine5"></span>IPixEngine5 interface</span></span>

<span data-ttu-id="c8d2b-104">Extensiones de la interfaz IPixEngine4 que contienen adiciones para ver las texturas.</span><span class="sxs-lookup"><span data-stu-id="c8d2b-104">Extensions to the IPixEngine4 interface containing additions for viewing textures.</span></span>

## <a name="members"></a><span data-ttu-id="c8d2b-105">Miembros</span><span class="sxs-lookup"><span data-stu-id="c8d2b-105">Members</span></span>

<span data-ttu-id="c8d2b-106">La interfaz **IPixEngine5** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="c8d2b-106">The **IPixEngine5** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="c8d2b-107">**IPixEngine5** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="c8d2b-107">**IPixEngine5** also has these types of members:</span></span>

-   [<span data-ttu-id="c8d2b-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="c8d2b-108">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="c8d2b-109"><span id="methods"></span>Métodos</span><span class="sxs-lookup"><span data-stu-id="c8d2b-109"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="c8d2b-110">La interfaz **IPixEngine5** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="c8d2b-110">The **IPixEngine5** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="c8d2b-111">Método</span><span class="sxs-lookup"><span data-stu-id="c8d2b-111">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="c8d2b-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="c8d2b-112">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="c8d2b-113"><a href="/windows/desktop/direct3dtools/ipixengine5-freetextureasync-uint-ipixengine5callbacks-ptr-dword-dword"><strong>FreeTextureAsync</strong></a></span><span class="sxs-lookup"><span data-stu-id="c8d2b-113"><a href="/windows/desktop/direct3dtools/ipixengine5-freetextureasync-uint-ipixengine5callbacks-ptr-dword-dword"><strong>FreeTextureAsync</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="c8d2b-114">Libera una textura y notifica al host de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="c8d2b-114">Frees a texture and notifies the host asynchronously.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="c8d2b-115"><a href="/windows/desktop/direct3dtools/ipixengine5-loadhistogramasync-uint-pixenginetexturesliceindex-int-bstr-ipixengine5callbacks-ptr-dword-dword"><strong>LoadHistogramAsync</strong></a></span><span class="sxs-lookup"><span data-stu-id="c8d2b-115"><a href="/windows/desktop/direct3dtools/ipixengine5-loadhistogramasync-uint-pixenginetexturesliceindex-int-bstr-ipixengine5callbacks-ptr-dword-dword"><strong>LoadHistogramAsync</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="c8d2b-116">Una solicitud asincrónica para cargar datos de histograma.</span><span class="sxs-lookup"><span data-stu-id="c8d2b-116">An asynchronous request to load histogram data.</span></span></p></td></tr><tr class="odd"><td style="text-align: left;"><span data-ttu-id="c8d2b-117"><a href="/windows/desktop/direct3dtools/ipixengine5-loadtexturefromfileasync-bstr-bstr-ipixengine5callbacks-ptr-dword-dword"><strong>LoadTextureFromFileAsync</strong></a></span><span class="sxs-lookup"><span data-stu-id="c8d2b-117"><a href="/windows/desktop/direct3dtools/ipixengine5-loadtexturefromfileasync-bstr-bstr-ipixengine5callbacks-ptr-dword-dword"><strong>LoadTextureFromFileAsync</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="c8d2b-118">Carga una textura desde un archivo y lo notifica al host de forma asincrónica cuando se completa.</span><span class="sxs-lookup"><span data-stu-id="c8d2b-118">Loads a texture from a file and notifies the host asynchronously when it completes.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="c8d2b-119"><a href="/windows/desktop/direct3dtools/ipixengine5-loadtexturesliceasync-uint-pixenginetexturesliceindex-int-bstr-ipixengine5callbacks-ptr-dword-dword"><strong>LoadTextureSliceAsync</strong></a></span><span class="sxs-lookup"><span data-stu-id="c8d2b-119"><a href="/windows/desktop/direct3dtools/ipixengine5-loadtexturesliceasync-uint-pixenginetexturesliceindex-int-bstr-ipixengine5callbacks-ptr-dword-dword"><strong>LoadTextureSliceAsync</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="c8d2b-120">Carga un segmento de textura y notifica al host asynchrnously cuando se completa.</span><span class="sxs-lookup"><span data-stu-id="c8d2b-120">Loads a texture slice and notifies the host asynchrnously when it completes.</span></span></p></td></tr><tr class="odd"><td style="text-align: left;"><span data-ttu-id="c8d2b-121"><a href="/windows/desktop/direct3dtools/ipixengine5-readtexelvalueasync-uint-pixenginetexturesliceindex-int-int-int-ipixengine5callbacks-ptr-dword-dword"><strong>ReadTexelValueAsync</strong></a></span><span class="sxs-lookup"><span data-stu-id="c8d2b-121"><a href="/windows/desktop/direct3dtools/ipixengine5-readtexelvalueasync-uint-pixenginetexturesliceindex-int-int-int-ipixengine5callbacks-ptr-dword-dword"><strong>ReadTexelValueAsync</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="c8d2b-122">Lee un valor textura y devuelve el resultado al host asynchrnously.</span><span class="sxs-lookup"><span data-stu-id="c8d2b-122">Reads a texel value and returns the result to the host asynchrnously.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="c8d2b-123"><a href="/previous-versions/windows/desktop/legacy/mt432769(v=vs.85)"><strong>RenderTextureAsync</strong></a></span><span class="sxs-lookup"><span data-stu-id="c8d2b-123"><a href="/previous-versions/windows/desktop/legacy/mt432769(v=vs.85)"><strong>RenderTextureAsync</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="c8d2b-124">Representa una textura en un archivo y devuelve el resultado al host asynchrnously.</span><span class="sxs-lookup"><span data-stu-id="c8d2b-124">Renders a texture to a file and returns the result to the host asynchrnously.</span></span></p></td></tr><tr class="odd"><td style="text-align: left;"><span data-ttu-id="c8d2b-125"><a href="/windows/desktop/direct3dtools/ipixengine5-savetextureasync-uint-bstr-ipixengine5callbacks-ptr-dword-dword"><strong>SaveTextureAsync</strong></a></span><span class="sxs-lookup"><span data-stu-id="c8d2b-125"><a href="/windows/desktop/direct3dtools/ipixengine5-savetextureasync-uint-bstr-ipixengine5callbacks-ptr-dword-dword"><strong>SaveTextureAsync</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="c8d2b-126">Guarda una textura.</span><span class="sxs-lookup"><span data-stu-id="c8d2b-126">Saves a texture.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="c8d2b-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c8d2b-127">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="c8d2b-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c8d2b-128">Header</span></span></p></td><td><span data-ttu-id="c8d2b-129">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="c8d2b-129">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
