---
description: La clase de identificador conocido \_ \_ hace referencia a una seudoclase en cada objeto WMI que indica la clase del objeto actual.
ms.assetid: a1d0e934-c5b5-4554-9d6e-3881064419ca
ms.tgt_platform: multiple
title: Identificador de __CLASS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0b4db6cacb6943619cf6468cf7f03d4a4c08278
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104156621"
---
# <a name="__class-identifier"></a><span data-ttu-id="faf7a-103">\_\_Identificador de clase</span><span class="sxs-lookup"><span data-stu-id="faf7a-103">\_\_CLASS Identifier</span></span>

<span data-ttu-id="faf7a-104">La clase de identificador conocido \_ \_ hace referencia a una seudoclase en cada objeto WMI que indica la clase del objeto actual.</span><span class="sxs-lookup"><span data-stu-id="faf7a-104">The well-known identifier \_\_CLASS refers to a pseudo-property on every WMI object that indicates the class of the current object.</span></span>

<span data-ttu-id="faf7a-105">Use \_ \_ la clase en una cláusula [Where](where-clause.md) para filtrar los objetos de clases derivadas del conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="faf7a-105">Use \_\_CLASS in a [WHERE](where-clause.md) clause to filter out any objects of derived classes from your result set.</span></span> <span data-ttu-id="faf7a-106">Por ejemplo, el conjunto de resultados de la siguiente consulta contiene no solo objetos cuya clase es [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk), sino también objetos cuya clase se deriva de **Win32 \_ LogicalDisk**.</span><span class="sxs-lookup"><span data-stu-id="faf7a-106">For example, the result set of the following query contains not only objects whose class is [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk), but also objects whose class is derived from **Win32\_LogicalDisk**.</span></span>


```sql
SELECT * FROM Win32_LogicalDisk
```



<span data-ttu-id="faf7a-107">En el ejemplo siguiente, el uso de la \_ \_ clase en la cláusula **Where** filtra todos los objetos de clases derivadas de [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) porque su clase no es de **Win32 \_ LogicalDisk**.</span><span class="sxs-lookup"><span data-stu-id="faf7a-107">In the following example, the use of \_\_CLASS in the **WHERE** clause filters out all objects of classes derived from [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) because their class is not **Win32\_LogicalDisk**.</span></span>


```sql
SELECT * FROM Win32_LogicalDisk   WHERE __CLASS = "Win32_LogicalDisk"
```



<span data-ttu-id="faf7a-108">Utilice \_ \_ la clase en proveedores que se solicitan para proporcionar instancias de una clase específica, con independencia de las subclases.</span><span class="sxs-lookup"><span data-stu-id="faf7a-108">Use \_\_CLASS in providers that are asked to provide instances of a specific class, irrespective of any subclasses.</span></span>

 

 
