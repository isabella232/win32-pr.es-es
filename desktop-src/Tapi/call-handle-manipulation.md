---
description: TAPI proporciona varias funciones para manipular los identificadores de llamada, determinar la relación entre las líneas, las llamadas y la dirección, etc.
ms.assetid: 283fe5e9-689f-4b87-97a6-b345c22ec6a2
title: Manipulación de identificadores de llamadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 248f16088f891b1441626097de5c803a8fe14991
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687246"
---
# <a name="call-handle-manipulation"></a><span data-ttu-id="707ac-103">Manipulación de identificadores de llamadas</span><span class="sxs-lookup"><span data-stu-id="707ac-103">Call Handle Manipulation</span></span>

<span data-ttu-id="707ac-104">TAPI proporciona varias funciones para manipular los identificadores de llamada, determinar la relación entre las líneas, las llamadas y la dirección, etc.</span><span class="sxs-lookup"><span data-stu-id="707ac-104">TAPI provides a number of functions for manipulating call handles, determining the relationship among lines, calls, and address, and so on.</span></span> <span data-ttu-id="707ac-105">La mayor parte de esta funcionalidad se implementa estrictamente en TAPI sin hacer referencia al proveedor de servicios, excepto para [**TSPI \_ lineGetCallAddressID**](/windows/win32/api/tspi/nf-tspi-tspi_linegetcalladdressid).</span><span class="sxs-lookup"><span data-stu-id="707ac-105">Most of this functionality is implemented strictly within TAPI without reference to the service provider, except for [**TSPI\_lineGetCallAddressID**](/windows/win32/api/tspi/nf-tspi-tspi_linegetcalladdressid).</span></span> <span data-ttu-id="707ac-106">Esta función recupera el identificador de dirección de una llamada existente dentro de su línea.</span><span class="sxs-lookup"><span data-stu-id="707ac-106">This function retrieves the address identifier of an existing call within its line.</span></span> <span data-ttu-id="707ac-107">Los proveedores de servicios que modelan una línea como un grupo de identificadores de direcciones pueden elegir una dirección imprevisible para una nueva llamada entrante o saliente.</span><span class="sxs-lookup"><span data-stu-id="707ac-107">Service providers that model a line as a group of address identifiers can choose an unpredictable address for a new inbound or outbound call.</span></span> <span data-ttu-id="707ac-108">Esta función proporciona información de TAPI suficiente para implementar la operación [**lineGetNewCalls**](/windows/win32/api/tapi/nf-tapi-linegetnewcalls) cuando se invoca con la opción de \_ Dirección LINECALLSELECT.</span><span class="sxs-lookup"><span data-stu-id="707ac-108">This function gives TAPI sufficient information to implement the [**lineGetNewCalls**](/windows/win32/api/tapi/nf-tapi-linegetnewcalls) operation when it is invoked with the LINECALLSELECT\_ADDRESS option.</span></span>

 

 
