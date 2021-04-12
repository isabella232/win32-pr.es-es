---
description: WMI utiliza las rutas de acceso de objeto en las propiedades de referencia de las clases de Asociación para identificar los objetos relacionados, así como el uso de rutas de acceso de objeto en parámetros de entrada o de salida para varios métodos.
ms.assetid: 07fee6f8-810e-4dec-8f0f-787756ee3beb
ms.tgt_platform: multiple
title: Requisitos de ruta de objeto WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2b46195eae3e8351c9c611a34c28cc9d5dd58d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423836"
---
# <a name="wmi-object-path-requirements"></a><span data-ttu-id="cf78c-103">Requisitos de ruta de objeto WMI</span><span class="sxs-lookup"><span data-stu-id="cf78c-103">WMI Object Path Requirements</span></span>

<span data-ttu-id="cf78c-104">WMI utiliza las rutas de acceso de objeto en las propiedades de referencia de las clases de Asociación para identificar los objetos relacionados, así como el uso de rutas de acceso de objeto en parámetros de entrada o de salida para varios métodos.</span><span class="sxs-lookup"><span data-stu-id="cf78c-104">WMI uses object paths in the reference properties of association classes to identify related objects, as well as using object paths in input or output parameters for several methods.</span></span> <span data-ttu-id="cf78c-105">Dado que las rutas de acceso a objetos se tratan como cadenas con fines de búsqueda y comparación, el valor de una ruta de acceso de objeto cuando se usa como propiedad de referencia es siempre la cadena en sí y no el objeto desreferenciado.</span><span class="sxs-lookup"><span data-stu-id="cf78c-105">Because object paths are treated as strings for the purpose of lookup and comparison, the value of an object path when used as a reference property is always the string itself and not the dereferenced object.</span></span> <span data-ttu-id="cf78c-106">Las comparaciones de cadenas que tratan las rutas de acceso a objetos siempre no distinguen mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="cf78c-106">String comparisons that deal with object paths are always case-insensitive.</span></span>

<span data-ttu-id="cf78c-107">Una ruta de acceso de objeto puede utilizar la siguiente sintaxis:</span><span class="sxs-lookup"><span data-stu-id="cf78c-107">An object path can use the following syntax:</span></span>

-   <span data-ttu-id="cf78c-108">Cadenas contenidas entre comillas simples.</span><span class="sxs-lookup"><span data-stu-id="cf78c-108">Strings contained in single quotation marks.</span></span>
-   <span data-ttu-id="cf78c-109">Las barras diagonales como separadores.</span><span class="sxs-lookup"><span data-stu-id="cf78c-109">Forward slashes as separators.</span></span>
-   <span data-ttu-id="cf78c-110">Barras diagonales inversas como separadores.</span><span class="sxs-lookup"><span data-stu-id="cf78c-110">Backslashes as separators.</span></span>
-   <span data-ttu-id="cf78c-111">Constantes hexadecimales para enteros.</span><span class="sxs-lookup"><span data-stu-id="cf78c-111">Hexadecimal constants for integers.</span></span>
-   <span data-ttu-id="cf78c-112">Constantes booleanas para las clases con claves que toman valores booleanos.</span><span class="sxs-lookup"><span data-stu-id="cf78c-112">Boolean constants for classes with keys that take Boolean values.</span></span>
-   <span data-ttu-id="cf78c-113">Notación de dirección URL que representa caracteres no imprimibles, como %20 para un espacio en blanco.</span><span class="sxs-lookup"><span data-stu-id="cf78c-113">URL notation to represent nonprinting characters, such as %20 for a blank space.</span></span>

<span data-ttu-id="cf78c-114">Además, una cadena de ruta de acceso de objeto debe cumplir las restricciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="cf78c-114">In addition, an object path string must obey the following restrictions:</span></span>

-   <span data-ttu-id="cf78c-115">Un servidor local asumido con una ruta de acceso de espacio de nombres parcial.</span><span class="sxs-lookup"><span data-stu-id="cf78c-115">An assumed local server with a partial namespace path.</span></span> <span data-ttu-id="cf78c-116">Por lo tanto, la especificación del espacio de nombres raíz y predeterminado implica el espacio de nombres raíz y predeterminado en el servidor local.</span><span class="sxs-lookup"><span data-stu-id="cf78c-116">Thus, specifying the root and default namespace implies the root and default namespace on the local server.</span></span>
-   <span data-ttu-id="cf78c-117">Ningún espacio en blanco dentro de un elemento o entre elementos.</span><span class="sxs-lookup"><span data-stu-id="cf78c-117">No white space either within an element or between elements.</span></span>
-   <span data-ttu-id="cf78c-118">Se permiten las comillas incrustadas en las rutas de acceso del objeto, pero debe delimitar la comilla con los caracteres de escape, como en una aplicación de C o C++.</span><span class="sxs-lookup"><span data-stu-id="cf78c-118">Embedded quotation marks in object paths are allowed but must delimit the quotation mark with escape characters, as in a C or C++ application.</span></span>
-   <span data-ttu-id="cf78c-119">Solo los valores decimales se reconocen como partes numéricas de las claves.</span><span class="sxs-lookup"><span data-stu-id="cf78c-119">Only decimal values are recognized as numeric portions of keys.</span></span>

 

 



