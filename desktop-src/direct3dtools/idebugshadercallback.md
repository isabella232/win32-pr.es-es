---
description: Devolución de llamada para devolver las instrucciones generadas a partir de la creación de un seguimiento de sombreador.
MS-HAID: vspixengine.IDebugShaderCallback
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Interfaz IDebugShaderCallback
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 9A4A3FD3-15E5-4DB5-8777-55797E32ABA3
api_name:
- IDebugShaderCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 676d76a0dbc199880badebc904a4eb66d2ad4d0e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105705212"
---
# <a name="span-idvspixengineidebugshadercallbackspanidebugshadercallback-interface"></a><span data-ttu-id="49ab5-103"><span id="vspixengine.idebugshadercallback"></span>Interfaz IDebugShaderCallback</span><span class="sxs-lookup"><span data-stu-id="49ab5-103"><span id="vspixengine.idebugshadercallback"></span>IDebugShaderCallback interface</span></span>

<span data-ttu-id="49ab5-104">Devolución de llamada para devolver las instrucciones generadas a partir de la creación de un seguimiento de sombreador.</span><span class="sxs-lookup"><span data-stu-id="49ab5-104">Callback to return the instructions generated from creating a shader trace.</span></span>

## <a name="members"></a><span data-ttu-id="49ab5-105">Miembros</span><span class="sxs-lookup"><span data-stu-id="49ab5-105">Members</span></span>

<span data-ttu-id="49ab5-106">La interfaz **IDebugShaderCallback** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="49ab5-106">The **IDebugShaderCallback** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="49ab5-107">**IDebugShaderCallback** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="49ab5-107">**IDebugShaderCallback** also has these types of members:</span></span>

-   [<span data-ttu-id="49ab5-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="49ab5-108">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="49ab5-109"><span id="methods"></span>Métodos</span><span class="sxs-lookup"><span data-stu-id="49ab5-109"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="49ab5-110">La interfaz **IDebugShaderCallback** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="49ab5-110">The **IDebugShaderCallback** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="49ab5-111">Método</span><span class="sxs-lookup"><span data-stu-id="49ab5-111">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="49ab5-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="49ab5-112">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="49ab5-113"><a href="/windows/desktop/direct3dtools/idebugshadercallback-resultinstructions-dword-byte-arr"><strong>ResultInstructions</strong></a></span><span class="sxs-lookup"><span data-stu-id="49ab5-113"><a href="/windows/desktop/direct3dtools/idebugshadercallback-resultinstructions-dword-byte-arr"><strong>ResultInstructions</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="49ab5-114">Devolución de llamada que notifica al host la información de instructrion devuelta por la solicitud asociada.</span><span class="sxs-lookup"><span data-stu-id="49ab5-114">A callback that notifies the host of instructrion information returned by the associated request.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="49ab5-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="49ab5-115">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="49ab5-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="49ab5-116">Header</span></span></p></td><td><span data-ttu-id="49ab5-117">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="49ab5-117">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
