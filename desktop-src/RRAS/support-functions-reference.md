---
title: Referencia de funciones de soporte
description: Las siguientes funciones se proporcionan a los protocolos de enrutamiento por parte del administrador de enrutadores.
ms.assetid: 4e88c9fe-f6ec-4f9c-88b1-8726e10d0f6d
keywords:
- Interfaz de protocolo de enrutamiento RRAS, funciones de soporte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbbaba49c5f7e4130491a50176d560ee565b0046
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104488070"
---
# <a name="support-functions-reference"></a><span data-ttu-id="34e9b-104">Referencia de funciones de soporte</span><span class="sxs-lookup"><span data-stu-id="34e9b-104">Support Functions Reference</span></span>

<span data-ttu-id="34e9b-105">Las siguientes funciones se proporcionan a los protocolos de enrutamiento por parte del administrador de enrutadores.</span><span class="sxs-lookup"><span data-stu-id="34e9b-105">The following functions are provided to routing protocols by the router manager.</span></span> <span data-ttu-id="34e9b-106">Cuando el administrador de enrutadores llama a la función [**StartProtocol**](/windows/desktop/api/Routprot/nc-routprot-pstart_protocol) (implementada por el protocolo de enrutamiento), el administrador de enrutadores pasa el protocolo de enrutamiento a una estructura de [**\_ funciones de soporte**](/windows/desktop/api/Routprot/ns-routprot-support_functions_50) que contiene punteros a estas funciones:</span><span class="sxs-lookup"><span data-stu-id="34e9b-106">When the router manager calls the [**StartProtocol**](/windows/desktop/api/Routprot/nc-routprot-pstart_protocol) function (implemented by the routing protocol), the router manager passes the routing protocol a [**SUPPORT\_FUNCTIONS**](/windows/desktop/api/Routprot/ns-routprot-support_functions_50) structure containing pointers to these functions:</span></span>

<span data-ttu-id="34e9b-107">[**DemandDialRequest**](/previous-versions/windows/desktop/legacy/aa373924(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="34e9b-107">[**DemandDialRequest**](/previous-versions/windows/desktop/legacy/aa373924(v=vs.85))</span></span>

<span data-ttu-id="34e9b-108">[**MIBEntryCreate**](/previous-versions/windows/desktop/legacy/aa374538(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="34e9b-108">[**MIBEntryCreate**](/previous-versions/windows/desktop/legacy/aa374538(v=vs.85))</span></span>

<span data-ttu-id="34e9b-109">[**MIBEntryDelete**](/previous-versions/windows/desktop/legacy/aa374539(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="34e9b-109">[**MIBEntryDelete**](/previous-versions/windows/desktop/legacy/aa374539(v=vs.85))</span></span>

<span data-ttu-id="34e9b-110">[**MIBEntryGet**](/previous-versions/windows/desktop/legacy/aa374540(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="34e9b-110">[**MIBEntryGet**](/previous-versions/windows/desktop/legacy/aa374540(v=vs.85))</span></span>

<span data-ttu-id="34e9b-111">[**MIBEntryGetFirst**](/previous-versions/windows/desktop/legacy/aa374541(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="34e9b-111">[**MIBEntryGetFirst**](/previous-versions/windows/desktop/legacy/aa374541(v=vs.85))</span></span>

<span data-ttu-id="34e9b-112">[**MIBEntryGetNext**](/previous-versions/windows/desktop/legacy/aa374542(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="34e9b-112">[**MIBEntryGetNext**](/previous-versions/windows/desktop/legacy/aa374542(v=vs.85))</span></span>

<span data-ttu-id="34e9b-113">[**MIBEntrySet**](/previous-versions/windows/desktop/legacy/aa374543(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="34e9b-113">[**MIBEntrySet**](/previous-versions/windows/desktop/legacy/aa374543(v=vs.85))</span></span>

<span data-ttu-id="34e9b-114">[**SetInterfaceReceiveType**](/previous-versions/windows/desktop/legacy/aa382181(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="34e9b-114">[**SetInterfaceReceiveType**](/previous-versions/windows/desktop/legacy/aa382181(v=vs.85))</span></span>

<span data-ttu-id="34e9b-115">[**ValidateRoute**](/previous-versions/windows/desktop/legacy/aa382342(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="34e9b-115">[**ValidateRoute**](/previous-versions/windows/desktop/legacy/aa382342(v=vs.85))</span></span>

 

 