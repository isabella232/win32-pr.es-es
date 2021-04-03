---
title: Ejemplos de cambios incompatibles
description: 'Cuando se trabaja con cambios incompatibles, la regla de control desafortunada es la siguiente: cualquier cambio puede ser incompatible con las versiones anteriores, a menos que sea muy bien entendido.'
ms.assetid: 5b893d79-b81d-4ede-8d49-71d85219c497
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9498e5c71c7ce9690da0969f234fbb9d094eca50
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075877"
---
# <a name="examples-of-incompatible-changes"></a><span data-ttu-id="ea638-103">Ejemplos de cambios incompatibles</span><span class="sxs-lookup"><span data-stu-id="ea638-103">Examples of Incompatible Changes</span></span>

<span data-ttu-id="ea638-104">Cuando se trabaja con cambios incompatibles, la regla de control de posición desafortunada es la siguiente: cualquier cambio puede ser incompatible con versiones anteriores, a menos que sea muy bien entendido.</span><span class="sxs-lookup"><span data-stu-id="ea638-104">When dealing with incompatible changes, the unfortunate rule of thumb is as follows: any change can be backward incompatible, unless it is very well understood.</span></span> <span data-ttu-id="ea638-105">Esta regla requiere conocimiento de las reglas de NDR.</span><span class="sxs-lookup"><span data-stu-id="ea638-105">This rule requires knowledge of NDR rules.</span></span> <span data-ttu-id="ea638-106">Si no sabe cuál es el NDR, no realice modificaciones.</span><span class="sxs-lookup"><span data-stu-id="ea638-106">If you do not know what the NDR is, do not make modifications.</span></span> <span data-ttu-id="ea638-107">Los ejemplos de cambios que normalmente producen una infracción de acceso en la aplicación, o una \_ excepción de datos de código auxiliar incorrecta \_ \_ generada por el motor de serialización, son las siguientes:</span><span class="sxs-lookup"><span data-stu-id="ea638-107">Examples of changes that typically result in an access violation in the application, or a BAD\_STUB\_DATA\_EXCEPTION raised by the marshaling engine, are as follows:</span></span>

-   <span data-ttu-id="ea638-108">Agregar un nuevo método en medio de métodos antiguos.</span><span class="sxs-lookup"><span data-stu-id="ea638-108">Adding a new method in the middle of old methods.</span></span>
-   <span data-ttu-id="ea638-109">Agregar o quitar parámetros de un método.</span><span class="sxs-lookup"><span data-stu-id="ea638-109">Adding or removing parameters from a method.</span></span>
-   <span data-ttu-id="ea638-110">Cambiar un atributo, por ejemplo un atributo de puntero: cambiar \[ ref \] a \[ Unique \] o PTR, \[ \] o viceversa.</span><span class="sxs-lookup"><span data-stu-id="ea638-110">Changing an attribute, for example a pointer attribute: changing \[ref\] to \[unique\] or \[ptr\] or vice versa.</span></span> <span data-ttu-id="ea638-111">Cada tipo de puntero tiene una representación de conexión diferente.</span><span class="sxs-lookup"><span data-stu-id="ea638-111">Each pointer type has a different wire representation.</span></span>
-   <span data-ttu-id="ea638-112">Cambiar el tamaño de los datos: de Short a Long, de char a WCHAR \_ t (Unicode), la adición de un campo a una estructura y el cambio del tamaño de una matriz de tamaño fijo.</span><span class="sxs-lookup"><span data-stu-id="ea638-112">Changing the size of the data: from short to long, from char to wchar\_t (unicode), adding a field to a structure, changing the size of a fixed size array.</span></span>
-   <span data-ttu-id="ea638-113">Agregar brazos de unión a una unión con una cláusula default.</span><span class="sxs-lookup"><span data-stu-id="ea638-113">Adding union arms to a union with a default clause.</span></span>

<span data-ttu-id="ea638-114">Algunos cambios dañinos o discrepancias no deseadas entre un cliente y un servidor se pueden producir de la manera siguiente:</span><span class="sxs-lookup"><span data-stu-id="ea638-114">Some insidious changes or unintended mismatches between a client and a server may occur as follows:</span></span>

-   <span data-ttu-id="ea638-115">Modificar un miembro de un tipo compuesto, como una estructura o una matriz.</span><span class="sxs-lookup"><span data-stu-id="ea638-115">Modifying a member of a compound type, like a structure or an array.</span></span> <span data-ttu-id="ea638-116">Por ejemplo, si un \_ identificador de cliente cambia de un entero a un GUID, una \_ estructura de registros de cliente con el \_ campo ID. de cliente es incompatible.</span><span class="sxs-lookup"><span data-stu-id="ea638-116">For example, if a CLIENT\_ID changes from an integral to a GUID, a CLIENT\_RECORD structure with the CLIENT\_ID field becomes incompatible.</span></span> <span data-ttu-id="ea638-117">Esto puede resultar difícil de detectar si está en cascada a través de varios niveles de inserción en un tipo de parámetro remoto real.</span><span class="sxs-lookup"><span data-stu-id="ea638-117">This may be difficult to detect if cascaded through several levels of embedding to an actual remote parameter type.</span></span>
-   <span data-ttu-id="ea638-118">Modificar un tipo importado.</span><span class="sxs-lookup"><span data-stu-id="ea638-118">Modifying an imported type.</span></span> <span data-ttu-id="ea638-119">Es posible que el tipo proceda de un componente diferente que no sea remoto directamente, por lo que se consideró que el cambio era compatible.</span><span class="sxs-lookup"><span data-stu-id="ea638-119">The type may be coming from a different component that does not remote directly, hence the change was thought to be compatible.</span></span>
-   <span data-ttu-id="ea638-120">\#El uso de ifdef en un archivo IDL es una idea mala de las definiciones de tipo en un archivo IDL, es un desastre en espera de producirse.</span><span class="sxs-lookup"><span data-stu-id="ea638-120">Using \#ifdef in an IDL file is a bad idea to ifdef type definitions in an IDL file—it is disaster waiting to happen.</span></span> <span data-ttu-id="ea638-121">Inevitablemente, debido a la compilación u otros problemas, un cliente se compila con un conjunto diferente de definiciones que el servidor y acaba siendo incompatible.</span><span class="sxs-lookup"><span data-stu-id="ea638-121">Inevitably, due to build or other glitches, a client is compiled with a different set of defines than the server, and they end up being incompatible.</span></span>

 

 




