---
description: Interfaz original para la comunicación de datos sobre un vsglog.
MS-HAID: vspixengine.IPixEngine
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Interfaz IPixEngine
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 87AB1D07-8E90-49F0-B44D-F6185923B8D4
api_name:
- IPixEngine
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 2f02538f7acbd88daf166af657382e507a4e5661
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104495736"
---
# <a name="span-idvspixengineipixenginespanipixengine-interface"></a><span data-ttu-id="bc9cc-103"><span id="vspixengine.ipixengine"></span>Interfaz IPixEngine</span><span class="sxs-lookup"><span data-stu-id="bc9cc-103"><span id="vspixengine.ipixengine"></span>IPixEngine interface</span></span>

<span data-ttu-id="bc9cc-104">Interfaz original para la comunicación de datos sobre un vsglog.</span><span class="sxs-lookup"><span data-stu-id="bc9cc-104">Original interface for communicating data about a vsglog .</span></span>

## <a name="members"></a><span data-ttu-id="bc9cc-105">Miembros</span><span class="sxs-lookup"><span data-stu-id="bc9cc-105">Members</span></span>

<span data-ttu-id="bc9cc-106">La interfaz **IPixEngine** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="bc9cc-106">The **IPixEngine** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="bc9cc-107">**IPixEngine** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="bc9cc-107">**IPixEngine** also has these types of members:</span></span>

-   [<span data-ttu-id="bc9cc-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="bc9cc-108">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="bc9cc-109"><span id="methods"></span>Métodos</span><span class="sxs-lookup"><span data-stu-id="bc9cc-109"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="bc9cc-110">La interfaz **IPixEngine** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="bc9cc-110">The **IPixEngine** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="bc9cc-111">Método</span><span class="sxs-lookup"><span data-stu-id="bc9cc-111">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="bc9cc-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="bc9cc-112">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="bc9cc-113"><a href="/windows/desktop/direct3dtools/ipixengine-openfile-bstr-bstr-inewframescallback-ptr-ifileiocallback-ptr-lcid"><strong>OpenFile</strong></a></span><span class="sxs-lookup"><span data-stu-id="bc9cc-113"><a href="/windows/desktop/direct3dtools/ipixengine-openfile-bstr-bstr-inewframescallback-ptr-ifileiocallback-ptr-lcid"><strong>OpenFile</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="bc9cc-114">Abre un registro de gráficos.</span><span class="sxs-lookup"><span data-stu-id="bc9cc-114">Opens a graphics log.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="bc9cc-115"><a href="/windows/desktop/direct3dtools/ipixengine-runexperiment-experiment-irunexperimentcallback-ptr-inewframescallback-ptr-ifileiocallback-ptr-dword-experimenttrigger-arr"><strong>RunExperiment</strong></a></span><span class="sxs-lookup"><span data-stu-id="bc9cc-115"><a href="/windows/desktop/direct3dtools/ipixengine-runexperiment-experiment-irunexperimentcallback-ptr-inewframescallback-ptr-ifileiocallback-ptr-dword-experimenttrigger-arr"><strong>RunExperiment</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="bc9cc-116">Ejecuta un experimento.</span><span class="sxs-lookup"><span data-stu-id="bc9cc-116">Runs an experiment.</span></span></p></td></tr><tr class="odd"><td style="text-align: left;"><span data-ttu-id="bc9cc-117"><a href="/windows/desktop/direct3dtools/ipixengine-savefile-bstr-ifileiocallback-ptr"><strong>SaveFile</strong></a></span><span class="sxs-lookup"><span data-stu-id="bc9cc-117"><a href="/windows/desktop/direct3dtools/ipixengine-savefile-bstr-ifileiocallback-ptr"><strong>SaveFile</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="bc9cc-118">Guarda el registro de gráficos en la ubicación especificada.</span><span class="sxs-lookup"><span data-stu-id="bc9cc-118">Saves the graphics log to the specified location.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="bc9cc-119"><a href="/windows/desktop/direct3dtools/ipixengine-setparentprocess-dword"><strong>SetParentProcess</strong></a></span><span class="sxs-lookup"><span data-stu-id="bc9cc-119"><a href="/windows/desktop/direct3dtools/ipixengine-setparentprocess-dword"><strong>SetParentProcess</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="bc9cc-120">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="bc9cc-120">Not used.</span></span></p></td></tr><tr class="odd"><td style="text-align: left;"><span data-ttu-id="bc9cc-121"><a href="/windows/desktop/direct3dtools/ipixengine-shutdown"><strong>Apagado</strong></a></span><span class="sxs-lookup"><span data-stu-id="bc9cc-121"><a href="/windows/desktop/direct3dtools/ipixengine-shutdown"><strong>ShutDown</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="bc9cc-122">Cierra el motor.</span><span class="sxs-lookup"><span data-stu-id="bc9cc-122">Shuts down the engine.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="bc9cc-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bc9cc-123">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="bc9cc-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bc9cc-124">Header</span></span></p></td><td><span data-ttu-id="bc9cc-125">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="bc9cc-125">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
