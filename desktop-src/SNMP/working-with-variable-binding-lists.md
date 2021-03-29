---
title: Trabajar con listas de enlaces de variables
description: Un enlace de variables es el emparejamiento de un nombre de instancia de objeto SNMP con un valor asociado. Una lista de enlaces de variables es una serie de entradas de enlace de variables. En WinSNMP, una unidad de datos de protocolo (PDU) incluye una lista de enlaces de variables.
ms.assetid: e6353ae7-1d32-4de4-8518-49864fcbfc57
keywords:
- Trabajar con listas de enlaces de variables SNMP
- El enlace de variables muestra SNMP, SNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26719c7dc987e61542f38a0b86db78c573793f98
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/20/2020
ms.locfileid: "103788889"
---
# <a name="working-with-variable-binding-lists"></a><span data-ttu-id="12a87-107">Trabajar con listas de enlaces de variables</span><span class="sxs-lookup"><span data-stu-id="12a87-107">Working with Variable Binding Lists</span></span>

<span data-ttu-id="12a87-108">Un *enlace de variables* es el emparejamiento de un nombre de instancia de objeto SNMP con un valor asociado.</span><span class="sxs-lookup"><span data-stu-id="12a87-108">A *variable binding* is the pairing of an SNMP object instance name with an associated value.</span></span> <span data-ttu-id="12a87-109">Una *lista de enlaces de variables* es una serie de entradas de enlace de variables.</span><span class="sxs-lookup"><span data-stu-id="12a87-109">A *variable binding list* is a series of variable binding entries.</span></span> <span data-ttu-id="12a87-110">En WinSNMP, una unidad de datos de protocolo (PDU) incluye una lista de enlaces de variables.</span><span class="sxs-lookup"><span data-stu-id="12a87-110">In WinSNMP, a protocol data unit (PDU) includes a variable binding list.</span></span>

<span data-ttu-id="12a87-111">Los detalles de la estructura de la lista de enlaces de variables están restringidos a la implementación de Microsoft WinSNMP.</span><span class="sxs-lookup"><span data-stu-id="12a87-111">The details of the variable binding list structure are restricted to the Microsoft WinSNMP implementation.</span></span> <span data-ttu-id="12a87-112">Una aplicación WinSNMP puede tener acceso a una lista de enlaces de variables con un identificador de tipo **HSNMP \_ VBL**.</span><span class="sxs-lookup"><span data-stu-id="12a87-112">A WinSNMP application can access a variable binding list with a handle of type **HSNMP\_VBL**.</span></span> <span data-ttu-id="12a87-113">Para obtener más información, vea [objetos de identificador de recursos](resource-handle-objects.md).</span><span class="sxs-lookup"><span data-stu-id="12a87-113">For more information, see [Resource Handle Objects](resource-handle-objects.md).</span></span>

<span data-ttu-id="12a87-114">La aplicación WinSNMP puede construir y manipular listas de enlaces de variables e incluirlas en PDU.</span><span class="sxs-lookup"><span data-stu-id="12a87-114">The WinSNMP application can construct and manipulate variable binding lists, and include them in PDUs.</span></span> <span data-ttu-id="12a87-115">Para realizar estas operaciones, la aplicación usa las [funciones de enlace de variables](winsnmp-functions.md)WinSNMP.</span><span class="sxs-lookup"><span data-stu-id="12a87-115">To perform these operations, the application uses the WinSNMP [variable binding functions](winsnmp-functions.md).</span></span> <span data-ttu-id="12a87-116">Para obtener más información sobre cómo trabajar con listas de enlaces WinSNMP y variables, vea los temas que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="12a87-116">For more information about working with WinSNMP and variable binding lists, see the topics listed in the following table.</span></span>



| <span data-ttu-id="12a87-117">Tema</span><span class="sxs-lookup"><span data-stu-id="12a87-117">Topic</span></span>                                                                    | <span data-ttu-id="12a87-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="12a87-118">Description</span></span>                                      |
|--------------------------------------------------------------------------|--------------------------------------------------|
| [<span data-ttu-id="12a87-119">Crear una lista de enlaces de variables</span><span class="sxs-lookup"><span data-stu-id="12a87-119">Creating a Variable Binding List</span></span>](creating-a-variable-binding-list.md) | <span data-ttu-id="12a87-120">Describe cómo crear una lista de enlaces de variables.</span><span class="sxs-lookup"><span data-stu-id="12a87-120">Describes how to create a variable binding list.</span></span> |
| [<span data-ttu-id="12a87-121">Administrar una lista de enlaces de variables</span><span class="sxs-lookup"><span data-stu-id="12a87-121">Managing a Variable Binding List</span></span>](managing-a-variable-binding-list.md) | <span data-ttu-id="12a87-122">Describe cómo administrar una lista de enlaces de variables.</span><span class="sxs-lookup"><span data-stu-id="12a87-122">Describes how to manage a variable binding list.</span></span> |



 

<span data-ttu-id="12a87-123">Para obtener más información sobre los enlaces de variables y listas de enlaces de variables, vea [RFC1905](https://www.ietf.org/rfc/rfc1905.txt), "operaciones de protocolo para la versión 2 del Protocolo simple de administración de redes (SNMPv2)" y las [funciones de enlace de variables](winsnmp-functions.md)WinSNMP.</span><span class="sxs-lookup"><span data-stu-id="12a87-123">For more information about variable bindings and variable binding lists, see [RFC1905](https://www.ietf.org/rfc/rfc1905.txt), "Protocol Operations for Version 2 of the Simple Network Management Protocol (SNMPv2)," and the WinSNMP [Variable Binding Functions](winsnmp-functions.md).</span></span>

 

 




