---
title: Sintaxis de nombre
description: Llamada a procedimiento remoto (RPC) y sintaxis de nombre.
ms.assetid: eb370106-bd88-4c21-b287-7b2b174185d4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d024130a5b8a873c6bfbb2194542344953625d5e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994411"
---
# <a name="name-syntax"></a><span data-ttu-id="7fbd9-103">Sintaxis de nombre</span><span class="sxs-lookup"><span data-stu-id="7fbd9-103">Name Syntax</span></span>

<span data-ttu-id="7fbd9-104">Microsoft RPC acepta nombres que se ajustan a la siguiente sintaxis:</span><span class="sxs-lookup"><span data-stu-id="7fbd9-104">Microsoft RPC accepts names that conform to the following syntax:</span></span>

``` syntax
/.:/name[/name...]/.../domainname/name[/name...]
```

## <a name="parameters"></a><span data-ttu-id="7fbd9-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7fbd9-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7fbd9-106"><span id="name"></span><span id="NAME"></span>Name</span><span class="sxs-lookup"><span data-stu-id="7fbd9-106"><span id="name"></span><span id="NAME"></span>name</span></span>
</dt> <dd>

<span data-ttu-id="7fbd9-107">Especifica un identificador que puede contener cualquier carácter excepto el carácter de barra diagonal (/) delimitador.</span><span class="sxs-lookup"><span data-stu-id="7fbd9-107">Specifies an identifier that can contain any character except the delimiting slash (/) character.</span></span>

</dd> <dt>

<span data-ttu-id="7fbd9-108"><span id="domainname"></span><span id="DOMAINNAME"></span>dominio de</span><span class="sxs-lookup"><span data-stu-id="7fbd9-108"><span id="domainname"></span><span id="DOMAINNAME"></span>domainname</span></span>
</dt> <dd>

<span data-ttu-id="7fbd9-109">Especifica el nombre del dominio.</span><span class="sxs-lookup"><span data-stu-id="7fbd9-109">Specifies the name of the domain.</span></span>

</dd> </dl>

<span data-ttu-id="7fbd9-110">Parámetro que selecciona el tipo de sintaxis de nombre y la cadena que especifica el nombre que se proporciona a muchas de las funciones RPC de la interfaz del servicio de nombres (NSI).</span><span class="sxs-lookup"><span data-stu-id="7fbd9-110">A parameter that selects the name-syntax type and the string that specifies the name are supplied to many of the name service interface (NSI) RPC functions.</span></span>

<span data-ttu-id="7fbd9-111">Microsoft RPC solo admite un tipo de sintaxis de nombre, tal y como se especifica en el \_ DCE de sintaxis de RPC C NS de constantes \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="7fbd9-111">Only one name-syntax type is supported by Microsoft RPC, as specified by the constant RPC\_C\_NS\_SYNTAX\_DCE.</span></span> <span data-ttu-id="7fbd9-112">Esta constante se define en el archivo de encabezado RPCNSI. H.</span><span class="sxs-lookup"><span data-stu-id="7fbd9-112">This constant is defined in the header file RPCNSI.H.</span></span>

<span data-ttu-id="7fbd9-113">La sintaxis de nombre especificada por \_ el \_ \_ DCE de sintaxis de RPC C NS \_ es una extensión de la \_ Sintaxis de nombre de servicio de directorio de celdas (CDs) de OSF DCE.</span><span class="sxs-lookup"><span data-stu-id="7fbd9-113">The name syntax specified by RPC\_C\_NS\_SYNTAX\_DCE is an extension of the OSF\_DCE Cell Directory Service (CDS) name syntax.</span></span> <span data-ttu-id="7fbd9-114">La capacidad de especificar un nombre de dominio representa una extensión de esa sintaxis.</span><span class="sxs-lookup"><span data-stu-id="7fbd9-114">The ability to specify a domain name represents an extension to that syntax.</span></span> <span data-ttu-id="7fbd9-115">No hay ningún límite absoluto en el número de nombres que se pueden separar con caracteres de barra diagonal, siempre y cuando la cadena global tenga menos de 256 caracteres.</span><span class="sxs-lookup"><span data-stu-id="7fbd9-115">There is no absolute limit on the number of names that can be separated by slash characters as long as the overall string is less than 256 characters.</span></span>

<span data-ttu-id="7fbd9-116">Las barras diagonales le permiten especificar una estructura lógica para el nombre, pero no se corresponden con una estructura lógica en los propios objetos.</span><span class="sxs-lookup"><span data-stu-id="7fbd9-116">The slashes allow you to specify a logical structure to the name, but they do not correspond to a logical structure in the objects themselves.</span></span>

 

 




