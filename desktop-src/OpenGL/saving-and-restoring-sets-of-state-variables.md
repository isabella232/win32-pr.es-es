---
title: Guardar y restaurar conjuntos de variables de estado
description: Puede guardar y restaurar los valores de una colección de variables de estado en una pila de atributos con las funciones glPushAttrib y glPopAttrib.
ms.assetid: 339de633-4158-4907-b985-2d75b465fb2a
keywords:
- Variables de estado de OpenGL
- guardar las variables de estado OpenGL
- restaurar variables de estado OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b3192c228ea35005c5755802d3cd1b873f7b7fe
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105665687"
---
# <a name="saving-and-restoring-sets-of-state-variables"></a><span data-ttu-id="df427-106">Guardar y restaurar conjuntos de variables de estado</span><span class="sxs-lookup"><span data-stu-id="df427-106">Saving and Restoring Sets of State Variables</span></span>

<span data-ttu-id="df427-107">Puede guardar y restaurar los valores de una colección de variables de estado en una pila de atributos con las funciones [**glPushAttrib**](glpushattrib.md) y [**glPopAttrib**](glpopattrib.md) .</span><span class="sxs-lookup"><span data-stu-id="df427-107">You can save and restore the values of a collection of state variables on an attribute stack with the [**glPushAttrib**](glpushattrib.md) and [**glPopAttrib**](glpopattrib.md) functions.</span></span> <span data-ttu-id="df427-108">La pila de atributo tiene una profundidad de 16 como mínimo.</span><span class="sxs-lookup"><span data-stu-id="df427-108">The attribute stack has a depth of at least 16.</span></span> <span data-ttu-id="df427-109">Para obtener la profundidad real, use la \_ profundidad máxima de la \_ \_ pila Max de GL \_ con [**glGetIntegerv**](glgetintegerv.md).</span><span class="sxs-lookup"><span data-stu-id="df427-109">To obtain the actual depth, use GL\_MAX\_ATTRIB\_STACK\_DEPTH with [**glGetIntegerv**](glgetintegerv.md).</span></span> <span data-ttu-id="df427-110">Si se inserta una pila completa o se extrae una vacía, se genera un error.</span><span class="sxs-lookup"><span data-stu-id="df427-110">Pushing a full stack or popping an empty one generates an error.</span></span>

<span data-ttu-id="df427-111">Por lo general, es más rápido usar **glPushAttrib** y **glPopAttrib** que para obtener y restaurar los valores.</span><span class="sxs-lookup"><span data-stu-id="df427-111">It is generally faster to use **glPushAttrib** and **glPopAttrib** than to get and restore the values yourself.</span></span> <span data-ttu-id="df427-112">Algunos valores se pueden insertar y extraer en el hardware, y guardarlos y restaurarlos puede consumir muchos recursos.</span><span class="sxs-lookup"><span data-stu-id="df427-112">Some values might be pushed and popped in the hardware, and saving and restoring them can be resource-intensive.</span></span> <span data-ttu-id="df427-113">Además, si está trabajando en un cliente remoto, todos los datos de atributo se deben transferir a través de la conexión de red y de nuevo a medida que se guardan y restauran.</span><span class="sxs-lookup"><span data-stu-id="df427-113">Also, if you're operating on a remote client, all of the attribute data must be transferred across the network connection and back as it is saved and restored.</span></span> <span data-ttu-id="df427-114">Sin embargo, la implementación de OpenGL mantiene la pila de atributo en el servidor, evitando los retrasos de red innecesarios.</span><span class="sxs-lookup"><span data-stu-id="df427-114">However, your OpenGL implementation keeps the attribute stack on the server, avoiding unnecessary network delays.</span></span>

<span data-ttu-id="df427-115">El prototipo de **glPushAttrib** es:</span><span class="sxs-lookup"><span data-stu-id="df427-115">The prototype of **glPushAttrib** is:</span></span>

<span data-ttu-id="df427-116">**void** **glPushAttrib**(**GLbitfield** *Mask* );</span><span class="sxs-lookup"><span data-stu-id="df427-116">**void** **glPushAttrib**(**GLbitfield** *mask* );</span></span>

<span data-ttu-id="df427-117">Al usar [**glPushAttrib**](glpushattrib.md) , se guardan todos los atributos indicados por bits en *Mask* y se insertan en la pila de atributos.</span><span class="sxs-lookup"><span data-stu-id="df427-117">Using [**glPushAttrib**](glpushattrib.md) saves all the attributes indicated by bits in *mask* by pushing them onto the attribute stack.</span></span> <span data-ttu-id="df427-118">Para obtener una lista de los posibles bits de máscara que puede realizar de forma lógica o conjunta para guardar cualquier combinación de atributos, consulte [grupos de atributos](attribute-groups.md).</span><span class="sxs-lookup"><span data-stu-id="df427-118">For a list of the possible mask bits you can logically OR together to save any combination of attributes, see [Attribute Groups](attribute-groups.md).</span></span> <span data-ttu-id="df427-119">Cada bit corresponde a una colección de variables de estado individuales.</span><span class="sxs-lookup"><span data-stu-id="df427-119">Each bit corresponds to a collection of individual state variables.</span></span> <span data-ttu-id="df427-120">Por ejemplo, el \_ bit de iluminación de GL \_ se refiere a todas las variables de estado relacionadas con la iluminación, que incluyen el color del material actual, el ambiente, la luz difusa, el reflejo y la luz emitida; una lista de las luces que están habilitadas y las direcciones de los focos.</span><span class="sxs-lookup"><span data-stu-id="df427-120">For example, GL\_LIGHTING\_BIT refers to all the state variables related to lighting, which include the current material color; the ambient, diffuse, specular, and emitted light; a list of the lights that are enabled; and the directions of the spotlights.</span></span> <span data-ttu-id="df427-121">Cuando se llama a [**glPopAttrib**](glpopattrib.md), se restauran todas las variables.</span><span class="sxs-lookup"><span data-stu-id="df427-121">When you call [**glPopAttrib**](glpopattrib.md), all those variables are restored.</span></span> <span data-ttu-id="df427-122">Para averiguar exactamente qué atributos se guardan para los valores de máscara concretos, consulte [variables de estado de OpenGL](opengl-state-variables.md).</span><span class="sxs-lookup"><span data-stu-id="df427-122">To find out exactly which attributes are saved for particular mask values, see [OpenGL State Variables](opengl-state-variables.md).</span></span>

 

 




