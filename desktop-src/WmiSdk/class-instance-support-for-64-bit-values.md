---
description: Proporciona restricciones para el uso de valores de 64 bits como parte de una ruta de acceso.
ms.assetid: 63f4f6c5-7803-425d-912f-bb1dd716e617
ms.tgt_platform: multiple
title: Compatibilidad de instancia de clase con valores de 64 bits
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 80f8a48f253cf2ef1902938ca6c54d01404b8466
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678165"
---
# <a name="class-instance-support-for-64-bit-values"></a><span data-ttu-id="de7cf-103">Compatibilidad de instancia de clase con valores de 64 bits</span><span class="sxs-lookup"><span data-stu-id="de7cf-103">Class Instance Support for 64-Bit Values</span></span>

<span data-ttu-id="de7cf-104">Puede usar un valor de clave de 64 bits como parte de una ruta de acceso, con las restricciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="de7cf-104">You can use a 64-bit key value as part of a path, with the following restrictions:</span></span>

-   <span data-ttu-id="de7cf-105">Siempre que no supere el intervalo de 32 bits, puede asignar y recuperar valores de la clave como lo haría con una propiedad de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="de7cf-105">As long as you do not exceed the 32-bit range, you can assign and retrieve values from the key as you would a 32-bit property.</span></span>
-   <span data-ttu-id="de7cf-106">Una vez superado el valor entero de 0x7FFFFFFF (para tipos con signo), 0x80000000 (para tipos sin signo) o 32 bits, debe usar comillas.</span><span class="sxs-lookup"><span data-stu-id="de7cf-106">After you exceed the integer value of 0x7FFFFFFF (for signed types), 0x80000000 (for unsigned types), or 32 bits, you must use quotation marks.</span></span>
-   <span data-ttu-id="de7cf-107">La única ruta de acceso válida para un valor de 64 bits se encuentra en las propiedades **\_ \_ RELPATH** o **\_ \_ path** de la instancia.</span><span class="sxs-lookup"><span data-stu-id="de7cf-107">The only valid path for a 64-bit value is located in the **\_\_RELPATH** or **\_\_PATH** properties of the instance.</span></span> <span data-ttu-id="de7cf-108">Como tal, WMI no admite la notación hexadecimal para el valor equivalente.</span><span class="sxs-lookup"><span data-stu-id="de7cf-108">As such, WMI does not support the hexadecimal notation for the equivalent value.</span></span>
-   <span data-ttu-id="de7cf-109">Si WMI registra la clave de instancia como un número negativo, debe utilizar el número original para recuperar la instancia.</span><span class="sxs-lookup"><span data-stu-id="de7cf-109">If WMI records the instance key as a negative number, then you must use the original number to retrieve the instance.</span></span>

<span data-ttu-id="de7cf-110">La semántica de consulta no se ve afectada y se comporta según lo esperado.</span><span class="sxs-lookup"><span data-stu-id="de7cf-110">Query semantics are unaffected and behave as expected.</span></span> <span data-ttu-id="de7cf-111">Este comportamiento solo afecta a las operaciones de ruta de acceso de objeto, [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject)y [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) .</span><span class="sxs-lookup"><span data-stu-id="de7cf-111">This behavior only affects the object path, [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject), and [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) operations.</span></span>

<span data-ttu-id="de7cf-112">En el ejemplo siguiente se muestra que las instancias de clase pueden tener valores de clave de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="de7cf-112">The following example shows that class instances can have 64-bit key values.</span></span>

``` syntax
class MyBig
{
  [key] sint64 k;
  sint64 p;
};

instance of MyBig
{
  k = 2;
  p = 3;
};
```

 

 



