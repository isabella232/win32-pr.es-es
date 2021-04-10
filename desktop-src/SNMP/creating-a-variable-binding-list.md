---
title: Crear una lista de enlaces de variables
description: La función SnmpCreateVbl crea una nueva lista de enlaces de variables.
ms.assetid: 18e8a04d-612f-4d85-9cff-8c541a4cdf71
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34e9ef7aa208e2e2f887d14c0e124f3bb659ff8f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268899"
---
# <a name="creating-a-variable-binding-list"></a><span data-ttu-id="89c9a-103">Crear una lista de enlaces de variables</span><span class="sxs-lookup"><span data-stu-id="89c9a-103">Creating a Variable Binding List</span></span>

<span data-ttu-id="89c9a-104">La función [**SnmpCreateVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatevbl) crea una nueva lista de enlaces de variables.</span><span class="sxs-lookup"><span data-stu-id="89c9a-104">The [**SnmpCreateVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatevbl) function creates a new variable binding list.</span></span> <span data-ttu-id="89c9a-105">Si la aplicación WinSNMP especifica un nombre de variable y un valor, la función crea la lista y agrega el nombre y el valor como la primera entrada de la lista.</span><span class="sxs-lookup"><span data-stu-id="89c9a-105">If the WinSNMP application specifies a variable name and a value, the function creates the list and adds the name and value as the first entry in the list.</span></span> <span data-ttu-id="89c9a-106">Si la aplicación especifica **null** para el nombre de la variable, la función crea una lista vacía.</span><span class="sxs-lookup"><span data-stu-id="89c9a-106">If the application specifies **NULL** for the variable name, the function creates an empty list.</span></span>

<span data-ttu-id="89c9a-107">Para copiar una lista de enlaces de variables, llame a la función [**SnmpDuplicateVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatevbl) .</span><span class="sxs-lookup"><span data-stu-id="89c9a-107">To copy a variable binding list, call the [**SnmpDuplicateVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatevbl) function.</span></span> <span data-ttu-id="89c9a-108">La función crea una nueva lista de enlaces de variables e inicializa la nueva lista con una copia de los datos en la lista de enlaces de variables de origen.</span><span class="sxs-lookup"><span data-stu-id="89c9a-108">The function creates a new variable binding list and initializes the new list with a copy of the data in the source variable binding list.</span></span>

<span data-ttu-id="89c9a-109">La función [**SnmpCreateVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatevbl) y la función [**SnmpDuplicateVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatevbl) asignan cualquier memoria necesaria para la nueva lista de enlaces de variables.</span><span class="sxs-lookup"><span data-stu-id="89c9a-109">The [**SnmpCreateVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatevbl) function and the [**SnmpDuplicateVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatevbl) function allocate any necessary memory for the new variable binding list.</span></span> <span data-ttu-id="89c9a-110">La aplicación WinSNMP debe liberar los recursos asociados a estas listas.</span><span class="sxs-lookup"><span data-stu-id="89c9a-110">The WinSNMP application must release the resources associated with these lists.</span></span> <span data-ttu-id="89c9a-111">Se recomienda que la aplicación haga esto coincidentes con cada llamada a [**SnmpCreateVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatevbl) y [**SnmpDuplicateVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatevbl) con la llamada correspondiente a la función [**SnmpFreeVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreevbl) cuando sea adecuado liberar la memoria asignada.</span><span class="sxs-lookup"><span data-stu-id="89c9a-111">It is recommended that the application do this by matching each call to [**SnmpCreateVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatevbl) and [**SnmpDuplicateVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatevbl) with a corresponding call to the [**SnmpFreeVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreevbl) function when it is appropriate to free the allocated memory.</span></span>

 

 




