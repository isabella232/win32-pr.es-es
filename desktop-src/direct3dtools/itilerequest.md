---
description: Solicitud de una textura en mosaico que se escribirá como un archivo DDS.
MS-HAID: vspixengine.ITileRequest
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Interfaz ITileRequest
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: DBA493E7-EBB6-490D-BDC6-946265A474D6
api_name:
- ITileRequest
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: ceb630661cfe67bc8beb28b2d1de2480726ec594
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103806253"
---
# <a name="span-idvspixengineitilerequestspanitilerequest-interface"></a><span data-ttu-id="e85b1-103"><span id="vspixengine.itilerequest"></span>Interfaz ITileRequest</span><span class="sxs-lookup"><span data-stu-id="e85b1-103"><span id="vspixengine.itilerequest"></span>ITileRequest interface</span></span>

<span data-ttu-id="e85b1-104">Solicitud de una textura en mosaico que se escribirá como un archivo DDS.</span><span class="sxs-lookup"><span data-stu-id="e85b1-104">Request for a tiled texture to be written as a DDS file.</span></span>

## <a name="members"></a><span data-ttu-id="e85b1-105">Miembros</span><span class="sxs-lookup"><span data-stu-id="e85b1-105">Members</span></span>

<span data-ttu-id="e85b1-106">La interfaz **ITileRequest** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="e85b1-106">The **ITileRequest** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="e85b1-107">**ITileRequest** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="e85b1-107">**ITileRequest** also has these types of members:</span></span>

-   [<span data-ttu-id="e85b1-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="e85b1-108">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="e85b1-109"><span id="methods"></span>Métodos</span><span class="sxs-lookup"><span data-stu-id="e85b1-109"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="e85b1-110">La interfaz **ITileRequest** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="e85b1-110">The **ITileRequest** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="e85b1-111">Método</span><span class="sxs-lookup"><span data-stu-id="e85b1-111">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="e85b1-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="e85b1-112">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="e85b1-113"><a href="/windows/desktop/direct3dtools/itilerequest-requestbuffertileasync-eventid-dword-bstr-uint-ibufferobjectdatacallback-ptr-dword-dword"><strong>RequestBufferTileAsync</strong></a></span><span class="sxs-lookup"><span data-stu-id="e85b1-113"><a href="/windows/desktop/direct3dtools/itilerequest-requestbuffertileasync-eventid-dword-bstr-uint-ibufferobjectdatacallback-ptr-dword-dword"><strong>RequestBufferTileAsync</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="e85b1-114">Solicita obtener el contenido sin procesar de un icono.</span><span class="sxs-lookup"><span data-stu-id="e85b1-114">Requests to get the raw contents of a tile.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="e85b1-115"><a href="/windows/desktop/direct3dtools/itilerequest-requesttexturetileasync-eventid-dword-uint-uint-uint-uint-bstr-itexturecallback-ptr-dword-dword"><strong>RequestTextureTileAsync</strong></a></span><span class="sxs-lookup"><span data-stu-id="e85b1-115"><a href="/windows/desktop/direct3dtools/itilerequest-requesttexturetileasync-eventid-dword-uint-uint-uint-uint-bstr-itexturecallback-ptr-dword-dword"><strong>RequestTextureTileAsync</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="e85b1-116">Solicita que obtenga el contenido de una textura en mosaico como. Archivo DDS (DirectDraw Surface).</span><span class="sxs-lookup"><span data-stu-id="e85b1-116">Requests to get the contents of a tiled texture as a .DDS (DirectDraw Surface) file.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="e85b1-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e85b1-117">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="e85b1-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e85b1-118">Header</span></span></p></td><td><span data-ttu-id="e85b1-119">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="e85b1-119">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
