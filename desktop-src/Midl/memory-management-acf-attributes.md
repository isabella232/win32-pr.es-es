---
title: Atributos ACF de administración de memoria
description: Los atributos que se enumeran en la tabla siguiente permiten realizar la administración de la memoria desde el lado cliente.
ms.assetid: ca03c7fe-6649-431b-89dc-5d07a3c8d591
keywords:
- ACF (MIDL), atributos, administración de memoria
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d12a0ee6d11a2b10e1c0fad7cd1a42411670b508
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103995200"
---
# <a name="memory-management-acf-attributes"></a><span data-ttu-id="d904c-104">Atributos ACF de administración de memoria</span><span class="sxs-lookup"><span data-stu-id="d904c-104">Memory Management ACF Attributes</span></span>

<span data-ttu-id="d904c-105">Los atributos que se enumeran en la tabla siguiente permiten realizar la administración de la memoria desde el lado cliente.</span><span class="sxs-lookup"><span data-stu-id="d904c-105">The attributes listed in the following table enable you to perform memory management from the client side.</span></span>



| <span data-ttu-id="d904c-106">Atributo</span><span class="sxs-lookup"><span data-stu-id="d904c-106">Attribute</span></span>                                   | <span data-ttu-id="d904c-107">Uso</span><span class="sxs-lookup"><span data-stu-id="d904c-107">Usage</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|---------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d904c-108">**allocate**</span><span class="sxs-lookup"><span data-stu-id="d904c-108">**allocate**</span></span>](allocate.md)                | <span data-ttu-id="d904c-109">Especifica el modo en que la aplicación cliente y el código auxiliar asignan y liberan memoria para los punteros.</span><span class="sxs-lookup"><span data-stu-id="d904c-109">Specifies the way the client application and stub allocate and release memory for pointers.</span></span> <span data-ttu-id="d904c-110">Este atributo es especialmente útil cuando se desea que ciertas estructuras de puntero sigan siendo accesibles para la aplicación de servidor después de que la llamada a procedimiento remoto se devuelva al cliente.</span><span class="sxs-lookup"><span data-stu-id="d904c-110">This attribute is particularly useful when you want certain pointer structures to remain accessible to the server application after the remote procedure call returns to the client.</span></span> <span data-ttu-id="d904c-111">También puede usar el atributo [**allocate**](allocate.md) para dirigir el código auxiliar para calcular el tamaño de toda la memoria a la que se hace referencia a través del puntero del tipo especificado y para hacer una llamada única a la [**\_ \_ asignación de usuarios de MIDL**](/windows/desktop/Rpc/the-midl-user-allocate-function).</span><span class="sxs-lookup"><span data-stu-id="d904c-111">You can also use the [**allocate**](allocate.md) attribute to direct the stub to compute the size of all memory referenced through the pointer of the specified type and to make a single call to [**midl\_user\_allocate**](/windows/desktop/Rpc/the-midl-user-allocate-function).</span></span> |
| [<span data-ttu-id="d904c-112">**recuento de bytes \_**</span><span class="sxs-lookup"><span data-stu-id="d904c-112">**byte\_count**</span></span>](byte-count.md)           | <span data-ttu-id="d904c-113">Permite crear un bloque persistente y contiguo de memoria que se puede reutilizar en varias llamadas a procedimientos remotos.</span><span class="sxs-lookup"><span data-stu-id="d904c-113">Enables you to create a persistent, contiguous block of memory that can be reused over multiple remote procedure calls.</span></span> <span data-ttu-id="d904c-114">Esto libera la aplicación cliente de la sobrecarga de la asignación y liberación repetidas de memoria que pueden incluir varios punteros y otras estructuras de datos complejas.</span><span class="sxs-lookup"><span data-stu-id="d904c-114">This frees the client application from the overhead of repeatedly allocating and releasing memory that may include multiple pointers and other complex data structures.</span></span>                                                                                                                                                                                                                                                      |
| [<span data-ttu-id="d904c-115">**habilitar \_ asignación**</span><span class="sxs-lookup"><span data-stu-id="d904c-115">**enable\_allocate**</span></span>](enable-allocate.md) | <span data-ttu-id="d904c-116">Especifica que el código auxiliar de servidor debe habilitar el entorno de administración de memoria de código auxiliar.</span><span class="sxs-lookup"><span data-stu-id="d904c-116">Specifies that the server stub code should enable the stub memory-management environment.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                            |



 

 

 