---
description: '<span id="vspixengine.ipipelinestagesrequest2"></span>Interfaz IPipeLineStagesRequest2: no se usa. Anteriormente, una solicitud de datos de fases de canalización.'
MS-HAID: vspixengine.IPipeLineStagesRequest2
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Interfaz IPipeLineStagesRequest2
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: B40E0701-3F17-4B3A-B150-D4B243662042
api_name:
- IPipeLineStagesRequest2
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: b9dd185ba709aa4439deb98f92be3c8f2f456cea
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107073"
---
# <a name="span-idvspixengineipipelinestagesrequest2spanipipelinestagesrequest2-interface"></a><span data-ttu-id="ab464-104"><span id="vspixengine.ipipelinestagesrequest2"></span>Interfaz IPipeLineStagesRequest2</span><span class="sxs-lookup"><span data-stu-id="ab464-104"><span id="vspixengine.ipipelinestagesrequest2"></span>IPipeLineStagesRequest2 interface</span></span>

<span data-ttu-id="ab464-105">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="ab464-105">Not used.</span></span> <span data-ttu-id="ab464-106">Anteriormente, una solicitud de datos de fases de canalización.</span><span class="sxs-lookup"><span data-stu-id="ab464-106">Formerly a request for pipeline stages data.</span></span>

## <a name="members"></a><span data-ttu-id="ab464-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="ab464-107">Members</span></span>

<span data-ttu-id="ab464-108">La **interfaz IPipeLineStagesRequest2** hereda de la [**interfaz IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)</span><span class="sxs-lookup"><span data-stu-id="ab464-108">The **IPipeLineStagesRequest2** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="ab464-109">**IPipeLineStagesRequest2** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="ab464-109">**IPipeLineStagesRequest2** also has these types of members:</span></span>

-   [<span data-ttu-id="ab464-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="ab464-110">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="ab464-111"><span id="methods"></span>Métodos</span><span class="sxs-lookup"><span data-stu-id="ab464-111"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="ab464-112">La **interfaz IPipeLineStagesRequest2** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="ab464-112">The **IPipeLineStagesRequest2** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="ab464-113">Método</span><span class="sxs-lookup"><span data-stu-id="ab464-113">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="ab464-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="ab464-114">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="ab464-115"><a href="/windows/desktop/direct3dtools/ipipelinestagesrequest2-requestcomputeshaderdataasync-eventid-ipipelinestagescallback2-ptr-dword-dword"><strong>RequestComputeShaderDataAsync</strong></a></span><span class="sxs-lookup"><span data-stu-id="ab464-115"><a href="/windows/desktop/direct3dtools/ipipelinestagesrequest2-requestcomputeshaderdataasync-eventid-ipipelinestagescallback2-ptr-dword-dword"><strong>RequestComputeShaderDataAsync</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="ab464-116">Una solicitud asincrónica para obtener datos del sombreador de proceso para el envío especificado.</span><span class="sxs-lookup"><span data-stu-id="ab464-116">An asynchronous request to get compute shader data for the specified dispatch.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="ab464-117"><a href="/windows/desktop/direct3dtools/ipipelinestagesrequest2-requestcomputeshaderstageasync-dword-eventid-ipipelinestagescallback-ptr-dword-dword"><strong>RequestComputeShaderStageAsync</strong></a></span><span class="sxs-lookup"><span data-stu-id="ab464-117"><a href="/windows/desktop/direct3dtools/ipipelinestagesrequest2-requestcomputeshaderstageasync-dword-eventid-ipipelinestagescallback-ptr-dword-dword"><strong>RequestComputeShaderStageAsync</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="ab464-118">Una solicitud asincrónica para obtener si se usó la fase del sombreador de proceso para el marco y el evento especificados.</span><span class="sxs-lookup"><span data-stu-id="ab464-118">An asynchronous request to get whether the compute shader stage was used for the specified frame and event.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="ab464-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ab464-119">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="ab464-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ab464-120">Header</span></span></p></td><td><span data-ttu-id="ab464-121">Vspixengine.h</span><span class="sxs-lookup"><span data-stu-id="ab464-121">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
