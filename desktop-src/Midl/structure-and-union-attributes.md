---
title: Atributos de estructura y de Unión
description: Use los \_ atributos switch \ para especificar la característica de una Unión en una llamada a procedimiento remoto. Utilice el atributo Ignore para designar determinados miembros de estructura o Unión como locales para la aplicación cliente.
ms.assetid: e06e5184-fa92-4446-964b-d56d0e5f2872
keywords:
- MIDL, atributos, estructura y Unión IDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b2a7764d56c8557bd71923021a9f324a118ac81
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104486734"
---
# <a name="structure-and-union-attributes"></a><span data-ttu-id="c9616-105">Atributos de estructura y de Unión</span><span class="sxs-lookup"><span data-stu-id="c9616-105">Structure and Union Attributes</span></span>

<span data-ttu-id="c9616-106">Utilice los **atributos \_ Switch** \* para especificar la característica de una Unión en una llamada a procedimiento remoto.</span><span class="sxs-lookup"><span data-stu-id="c9616-106">Use the **switch\_**\* attributes to specify the characteristic of a union in a remote procedure call.</span></span> <span data-ttu-id="c9616-107">Utilice el atributo [**Ignore**](ignore.md) para designar determinados miembros de estructura o Unión como locales para la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="c9616-107">Use the [**ignore**](ignore.md) attribute to designate certain structure or union members as local to the client application.</span></span>



| <span data-ttu-id="c9616-108">Atributo</span><span class="sxs-lookup"><span data-stu-id="c9616-108">Attribute</span></span>                           | <span data-ttu-id="c9616-109">Uso</span><span class="sxs-lookup"><span data-stu-id="c9616-109">Usage</span></span>                                                                                                                         |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c9616-110">**switch**</span><span class="sxs-lookup"><span data-stu-id="c9616-110">**switch**</span></span>](switch.md)            | <span data-ttu-id="c9616-111">Selecciona el discriminante de una Unión encapsulada.</span><span class="sxs-lookup"><span data-stu-id="c9616-111">Selects the discriminant for an encapsulated union.</span></span>                                                                           |
| [<span data-ttu-id="c9616-112">**el modificador \_ es**</span><span class="sxs-lookup"><span data-stu-id="c9616-112">**switch\_is**</span></span>](switch-is.md)     | <span data-ttu-id="c9616-113">Identifica discriminante para una Unión no encapsulada.</span><span class="sxs-lookup"><span data-stu-id="c9616-113">Identifies the discriminant for a nonencapsulated union.</span></span>                                                                      |
| [<span data-ttu-id="c9616-114">**tipo de conmutador \_**</span><span class="sxs-lookup"><span data-stu-id="c9616-114">**switch\_type**</span></span>](switch-type.md) | <span data-ttu-id="c9616-115">Identifica el tipo de discriminante para una Unión no encapsulada.</span><span class="sxs-lookup"><span data-stu-id="c9616-115">Identifies the type of the discriminant for a nonencapsulated union.</span></span>                                                          |
| [<span data-ttu-id="c9616-116">**omitir**</span><span class="sxs-lookup"><span data-stu-id="c9616-116">**ignore**</span></span>](ignore.md)            | <span data-ttu-id="c9616-117">Designa que un puntero contenido en una estructura o Unión y el objeto indicado por el puntero no se va a transmitir.</span><span class="sxs-lookup"><span data-stu-id="c9616-117">Designates that a pointer contained in a structure or union and the object indicated by the pointer is not to be transmitted.</span></span> |



 

<span data-ttu-id="c9616-118">También puede usar los [atributos de puntero de matriz y tamaño](array-and-sized-pointer-attributes.md) para especificar características de miembros de estructura o Unión.</span><span class="sxs-lookup"><span data-stu-id="c9616-118">You can also use the [array and sized pointer attributes](array-and-sized-pointer-attributes.md) to specify characteristics of structure or union members.</span></span>

 

 




