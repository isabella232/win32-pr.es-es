---
description: 'Solicitud para iniciar la depuración de un sombreador. Esta solicitud contiene dos partes: generar un seguimiento y depurar un seguimiento.'
MS-HAID: vspixengine.IDebugShaderRequest2
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Interfaz IDebugShaderRequest2
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 80F95900-F2E6-4B5C-B902-573280956E94
api_name:
- IDebugShaderRequest2
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 7b7c183cc04422d47b8d6599c67f2e7c1f5e58cd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152370"
---
# <a name="span-idvspixengineidebugshaderrequest2spanidebugshaderrequest2-interface"></a><span data-ttu-id="fdee4-104"><span id="vspixengine.idebugshaderrequest2"></span>Interfaz IDebugShaderRequest2</span><span class="sxs-lookup"><span data-stu-id="fdee4-104"><span id="vspixengine.idebugshaderrequest2"></span>IDebugShaderRequest2 interface</span></span>

<span data-ttu-id="fdee4-105">Solicitud para iniciar la depuración de un sombreador.</span><span class="sxs-lookup"><span data-stu-id="fdee4-105">Request to start debugging a shader.</span></span> <span data-ttu-id="fdee4-106">Esta solicitud contiene dos partes: generar un seguimiento y depurar un seguimiento.</span><span class="sxs-lookup"><span data-stu-id="fdee4-106">This request contains two parts: generate a trace, and debug a trace.</span></span>

## <a name="members"></a><span data-ttu-id="fdee4-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="fdee4-107">Members</span></span>

<span data-ttu-id="fdee4-108">La interfaz **IDebugShaderRequest2** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="fdee4-108">The **IDebugShaderRequest2** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="fdee4-109">**IDebugShaderRequest2** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="fdee4-109">**IDebugShaderRequest2** also has these types of members:</span></span>

-   [<span data-ttu-id="fdee4-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="fdee4-110">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="fdee4-111"><span id="methods"></span>Métodos</span><span class="sxs-lookup"><span data-stu-id="fdee4-111"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="fdee4-112">La interfaz **IDebugShaderRequest2** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="fdee4-112">The **IDebugShaderRequest2** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="fdee4-113">Método</span><span class="sxs-lookup"><span data-stu-id="fdee4-113">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="fdee4-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="fdee4-114">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="fdee4-115"><a href="/windows/desktop/direct3dtools/idebugshaderrequest2-begindebugshader-ipixerrorcallback-ptr-dword-byte-arr-dword-ptr"><strong>BeginDebugShader</strong></a></span><span class="sxs-lookup"><span data-stu-id="fdee4-115"><a href="/windows/desktop/direct3dtools/idebugshaderrequest2-begindebugshader-ipixerrorcallback-ptr-dword-byte-arr-dword-ptr"><strong>BeginDebugShader</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="fdee4-116">Solicita que inicie la depuración de la lista de instrucciones especificada.</span><span class="sxs-lookup"><span data-stu-id="fdee4-116">Requests to start debugging the specified list of instructions.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="fdee4-117"><a href="/windows/desktop/direct3dtools/idebugshaderrequest2-generateinstructions-ipixerrorcallback-ptr-debugshaderrequestinfo-ptr-pixelhistoryoperation-ptr-idebugshadercallback-ptr"><strong>GenerateInstructions</strong></a></span><span class="sxs-lookup"><span data-stu-id="fdee4-117"><a href="/windows/desktop/direct3dtools/idebugshaderrequest2-generateinstructions-ipixerrorcallback-ptr-debugshaderrequestinfo-ptr-pixelhistoryoperation-ptr-idebugshadercallback-ptr"><strong>GenerateInstructions</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="fdee4-118">Solicitudes para generar instrucciones de seguimiento del sombreador en una solicitud de depuración.</span><span class="sxs-lookup"><span data-stu-id="fdee4-118">Requests to generate shader trace instructions in a debug request.</span></span> <span data-ttu-id="fdee4-119">La depuración basada en seguimiento se produce en la CPU (warp) en lugar de en la GPU.</span><span class="sxs-lookup"><span data-stu-id="fdee4-119">Trace-based debugging occurs on the CPU (warp) instead of the GPU.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="fdee4-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fdee4-120">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="fdee4-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fdee4-121">Header</span></span></p></td><td><span data-ttu-id="fdee4-122">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="fdee4-122">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
