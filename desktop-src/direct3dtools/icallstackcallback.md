---
description: Devolución de llamada para devolver datos de pila de llamadas.
MS-HAID: vspixengine.ICallStackCallback
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Interfaz ICallStackCallback
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: AF380634-A284-4DCA-B746-FB1D8BE099B4
api_name:
- ICallStackCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: db6b2aa72008d11891c211512308290a3393ee49
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103806218"
---
# <a name="span-idvspixengineicallstackcallbackspanicallstackcallback-interface"></a><span data-ttu-id="c2bfe-103"><span id="vspixengine.icallstackcallback"></span>Interfaz ICallStackCallback</span><span class="sxs-lookup"><span data-stu-id="c2bfe-103"><span id="vspixengine.icallstackcallback"></span>ICallStackCallback interface</span></span>

<span data-ttu-id="c2bfe-104">Devolución de llamada para devolver datos de pila de llamadas.</span><span class="sxs-lookup"><span data-stu-id="c2bfe-104">Callback to return callstack data.</span></span>

## <a name="members"></a><span data-ttu-id="c2bfe-105">Miembros</span><span class="sxs-lookup"><span data-stu-id="c2bfe-105">Members</span></span>

<span data-ttu-id="c2bfe-106">La interfaz **ICallStackCallback** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="c2bfe-106">The **ICallStackCallback** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="c2bfe-107">**ICallStackCallback** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="c2bfe-107">**ICallStackCallback** also has these types of members:</span></span>

-   [<span data-ttu-id="c2bfe-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="c2bfe-108">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="c2bfe-109"><span id="methods"></span>Métodos</span><span class="sxs-lookup"><span data-stu-id="c2bfe-109"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="c2bfe-110">La interfaz **ICallStackCallback** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="c2bfe-110">The **ICallStackCallback** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="c2bfe-111">Método</span><span class="sxs-lookup"><span data-stu-id="c2bfe-111">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="c2bfe-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="c2bfe-112">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="c2bfe-113"><a href="/windows/desktop/direct3dtools/icallstackcallback-resultcallback-dword-callstackframe-arr"><strong>ResultCallback</strong></a></span><span class="sxs-lookup"><span data-stu-id="c2bfe-113"><a href="/windows/desktop/direct3dtools/icallstackcallback-resultcallback-dword-callstackframe-arr"><strong>ResultCallback</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="c2bfe-114">Función de devolución de llamada que se usa para notificar al host la información de la pila de llamadas.</span><span class="sxs-lookup"><span data-stu-id="c2bfe-114">A callback function used to notify the host of call stack information.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="c2bfe-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c2bfe-115">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="c2bfe-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c2bfe-116">Header</span></span></p></td><td><span data-ttu-id="c2bfe-117">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="c2bfe-117">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
