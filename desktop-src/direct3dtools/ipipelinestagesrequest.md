---
description: No se utiliza. Anteriormente, una solicitud de datos de etapas de canalización.
MS-HAID: vspixengine.IPipeLineStagesRequest
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Interfaz IPipeLineStagesRequest
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 5D6EB81F-F60F-49CF-9F34-FABDA05ED3F8
api_name:
- IPipeLineStagesRequest
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 4dfa67e0770b1c709ee80bffd01831859ad4c45a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105705239"
---
# <a name="span-idvspixengineipipelinestagesrequestspanipipelinestagesrequest-interface"></a><span data-ttu-id="a2ad8-104"><span id="vspixengine.ipipelinestagesrequest"></span>Interfaz IPipeLineStagesRequest</span><span class="sxs-lookup"><span data-stu-id="a2ad8-104"><span id="vspixengine.ipipelinestagesrequest"></span>IPipeLineStagesRequest interface</span></span>

<span data-ttu-id="a2ad8-105">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="a2ad8-105">Not used.</span></span> <span data-ttu-id="a2ad8-106">Anteriormente, una solicitud de datos de etapas de canalización.</span><span class="sxs-lookup"><span data-stu-id="a2ad8-106">Formerly a request for pipeline stages data.</span></span>

## <a name="members"></a><span data-ttu-id="a2ad8-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="a2ad8-107">Members</span></span>

<span data-ttu-id="a2ad8-108">La interfaz **IPipeLineStagesRequest** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="a2ad8-108">The **IPipeLineStagesRequest** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="a2ad8-109">**IPipeLineStagesRequest** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="a2ad8-109">**IPipeLineStagesRequest** also has these types of members:</span></span>

-   [<span data-ttu-id="a2ad8-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="a2ad8-110">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="a2ad8-111"><span id="methods"></span>Métodos</span><span class="sxs-lookup"><span data-stu-id="a2ad8-111"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="a2ad8-112">La interfaz **IPipeLineStagesRequest** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="a2ad8-112">The **IPipeLineStagesRequest** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="a2ad8-113">Método</span><span class="sxs-lookup"><span data-stu-id="a2ad8-113">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="a2ad8-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="a2ad8-114">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="a2ad8-115"><a href="/windows/desktop/direct3dtools/ipipelinestagesrequest-requestasync-eventid-dword-pipelinestagesid-arr-dword-dword-ipipelinestagescallback-ptr-bool-dword-dword"><strong>RequestAsync</strong></a></span><span class="sxs-lookup"><span data-stu-id="a2ad8-115"><a href="/windows/desktop/direct3dtools/ipipelinestagesrequest-requestasync-eventid-dword-pipelinestagesid-arr-dword-dword-ipipelinestagescallback-ptr-bool-dword-dword"><strong>RequestAsync</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="a2ad8-116">Una solicitud asincrónica para obtener las imágenes de vista previa para la ventana etapas de canalización de gráficos.</span><span class="sxs-lookup"><span data-stu-id="a2ad8-116">An asynchronous request to get preview images for the graphics pipeline stages window.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="a2ad8-117"><a href="/windows/desktop/direct3dtools/ipipelinestagesrequest-requestsupportedstagesasync-dword-eventid-ipipelinestagescallback-ptr-dword-dword"><strong>RequestSupportedStagesAsync</strong></a></span><span class="sxs-lookup"><span data-stu-id="a2ad8-117"><a href="/windows/desktop/direct3dtools/ipipelinestagesrequest-requestsupportedstagesasync-dword-eventid-ipipelinestagescallback-ptr-dword-dword"><strong>RequestSupportedStagesAsync</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="a2ad8-118">Una solicitud asincrónica para obtener una lista de las fases usadas para el marco y el evento especificados.</span><span class="sxs-lookup"><span data-stu-id="a2ad8-118">An asynchronous request to get a list of stages used for the specified frame and event.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="a2ad8-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a2ad8-119">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="a2ad8-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a2ad8-120">Header</span></span></p></td><td><span data-ttu-id="a2ad8-121">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="a2ad8-121">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
