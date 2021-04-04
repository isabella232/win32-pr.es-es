---
title: Administrar una lista de enlaces de variables
description: La función SnmpGetVb recupera información de enlace de variables de una lista de enlaces de variables. La función recupera el nombre de la variable y el valor asociado de la variable de la entrada de enlace de variables especificada por la aplicación WinSNMP.
ms.assetid: 357aebd6-171a-4221-b12a-712702f9d9c6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cc8c1cbfa4eb0ec3acdc13e9c9cc480b88ddae8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075475"
---
# <a name="managing-a-variable-binding-list"></a><span data-ttu-id="e1391-104">Administrar una lista de enlaces de variables</span><span class="sxs-lookup"><span data-stu-id="e1391-104">Managing a Variable Binding List</span></span>

<span data-ttu-id="e1391-105">La función [**SnmpGetVb**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetvb) recupera información de enlace de variables de una lista de enlaces de variables.</span><span class="sxs-lookup"><span data-stu-id="e1391-105">The [**SnmpGetVb**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetvb) function retrieves variable binding information from a variable binding list.</span></span> <span data-ttu-id="e1391-106">La función recupera el nombre de la variable y el valor asociado de la variable de la entrada de enlace de variables especificada por la aplicación WinSNMP.</span><span class="sxs-lookup"><span data-stu-id="e1391-106">The function retrieves the variable name and the variable's associated value from the variable binding entry specified by the WinSNMP application.</span></span>

<span data-ttu-id="e1391-107">Para actualizar las entradas de enlace de variables en una lista de enlaces de variables, llame a la función [**SnmpSetVb**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetvb) .</span><span class="sxs-lookup"><span data-stu-id="e1391-107">To update variable binding entries in a variable binding list, call the [**SnmpSetVb**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetvb) function.</span></span> <span data-ttu-id="e1391-108">La función **SnmpSetVb** también anexa nuevas entradas de enlace de variables a una lista de enlaces de variables existente.</span><span class="sxs-lookup"><span data-stu-id="e1391-108">The **SnmpSetVb** function also appends new variable binding entries to an existing variable binding list.</span></span>

<span data-ttu-id="e1391-109">La aplicación WinSNMP debe llamar a la función [**SnmpDeleteVb**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpdeletevb) para quitar las entradas de una lista de enlaces de variables.</span><span class="sxs-lookup"><span data-stu-id="e1391-109">The WinSNMP application must call the [**SnmpDeleteVb**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpdeletevb) function to remove entries from a variable binding list.</span></span>

<span data-ttu-id="e1391-110">Para recuperar, modificar o eliminar una entrada de enlace de variables, la aplicación WinSNMP debe especificar la posición de la entrada en la lista de enlaces de variables.</span><span class="sxs-lookup"><span data-stu-id="e1391-110">To retrieve, modify or delete a variable binding entry, the WinSNMP application must specify the position of the entry in the variable binding list.</span></span>

<span data-ttu-id="e1391-111">Una llamada a la función [**SnmpSetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata) asocia una lista de enlaces de variables a una PDU.</span><span class="sxs-lookup"><span data-stu-id="e1391-111">A call to the [**SnmpSetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata) function associates a variable binding list with a PDU.</span></span> <span data-ttu-id="e1391-112">Una llamada a la función [**SnmpGetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetpdudata) recupera una lista de enlaces de variables de una PDU.</span><span class="sxs-lookup"><span data-stu-id="e1391-112">A call to the [**SnmpGetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetpdudata) function retrieves a variable binding list from a PDU.</span></span> <span data-ttu-id="e1391-113">Un enlace de variable individual no está asociado directamente a una PDU, pero se asocia indirectamente a través de su inclusión en una lista de enlaces de variables.</span><span class="sxs-lookup"><span data-stu-id="e1391-113">An individual variable binding is not directly associated with a PDU, but it is indirectly associated through its inclusion in a variable binding list.</span></span>

 

 




