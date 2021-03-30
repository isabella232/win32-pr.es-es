---
description: Un analizador es el Monitor de red componente que inspecciona los datos en una captura diferida y pasa información de protocolo específica a la aplicación que llama al analizador. Un analizador es pasivo porque solo funciona cuando Monitor de red o un experto lo llama.
ms.assetid: 6c135a24-5718-429a-988b-a2abd6b563d1
title: Analizador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74aa86a17e87ab139ad48583285da943f23d330c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907661"
---
# <a name="parser"></a><span data-ttu-id="fadd1-104">Analizador</span><span class="sxs-lookup"><span data-stu-id="fadd1-104">Parser</span></span>

<span data-ttu-id="fadd1-105">Un analizador es el Monitor de red componente que inspecciona los datos en una [*captura diferida*](d.md)y pasa información de protocolo específica a la aplicación que llama al analizador.</span><span class="sxs-lookup"><span data-stu-id="fadd1-105">A parser is the Network Monitor component that inspects data in a [*delayed capture*](d.md), and passes specific protocol information to the application that calls the parser.</span></span> <span data-ttu-id="fadd1-106">Un analizador es pasivo porque solo funciona cuando Monitor de red o un [*experto*](e.md) lo llama.</span><span class="sxs-lookup"><span data-stu-id="fadd1-106">A parser is passive because it works only when Network Monitor or an [*expert*](e.md) call it.</span></span>

<span data-ttu-id="fadd1-107">Cada analizador identifica un protocolo y, normalmente, se implementa un analizador dentro de su propio archivo DLL de analizador.</span><span class="sxs-lookup"><span data-stu-id="fadd1-107">Each parser identifies one protocol, and typically, a parser is implemented within its own parser DLL.</span></span> <span data-ttu-id="fadd1-108">Sin embargo, un archivo DLL de analizador puede contener varios analizadores, lo que significa que se puede usar una DLL para detectar más de un protocolo.</span><span class="sxs-lookup"><span data-stu-id="fadd1-108">However, a parser DLL can contain multiple parsers which means that one DLL can be used to detect more than one protocol.</span></span>

<span data-ttu-id="fadd1-109">Los datos que se pasan a un analizador se toman de una [*captura diferida*](d.md)y se pasan al analizador fotograma a fotograma.</span><span class="sxs-lookup"><span data-stu-id="fadd1-109">The data passed to a parser is taken from a [*delayed capture*](d.md), and passed to the parser on a frame-by-frame basis.</span></span> <span data-ttu-id="fadd1-110">No se puede analizar una captura en tiempo real.</span><span class="sxs-lookup"><span data-stu-id="fadd1-110">You cannot parse a real-time capture.</span></span>

<span data-ttu-id="fadd1-111">Para analizar los datos de un marco, el analizador debe reconocer la instancia del Protocolo, identificar las propiedades que existen en la instancia del protocolo y adjuntar una definición de propiedad a cada propiedad.</span><span class="sxs-lookup"><span data-stu-id="fadd1-111">To parse the data in a frame, the parser must recognize the protocol instance, identify the properties that exist in the protocol instance, and attach a property definition to each property.</span></span> <span data-ttu-id="fadd1-112">Tenga en cuenta que el marco solo contiene un flujo de datos.</span><span class="sxs-lookup"><span data-stu-id="fadd1-112">Be aware that the frame contains only a stream of data.</span></span> <span data-ttu-id="fadd1-113">El marco no contiene datos que indiquen qué protocolos o propiedades de protocolo representan los datos.</span><span class="sxs-lookup"><span data-stu-id="fadd1-113">The frame does not contain data that indicates which protocols or protocol properties the data represents.</span></span>

<span data-ttu-id="fadd1-114">En la ilustración siguiente se muestra un marco que contiene una instancia de un protocolo.</span><span class="sxs-lookup"><span data-stu-id="fadd1-114">The following illustration shows a frame that contains an instance of a protocol.</span></span>

![marco que contiene una instancia de protocolo](images/parser1.png)

<span data-ttu-id="fadd1-116">Si Monitor de red va a mostrar los datos analizados en la interfaz de usuario, el analizador debe dar formato a los datos.</span><span class="sxs-lookup"><span data-stu-id="fadd1-116">If Network Monitor is going to display parsed data in the UI, the parser must format the data.</span></span> <span data-ttu-id="fadd1-117">Sin embargo, algunos expertos usan el resultado del analizador mediante programación y no muestran el resultado en la interfaz de usuario de Monitor de red.</span><span class="sxs-lookup"><span data-stu-id="fadd1-117">However, some experts use the parser output programmatically, and do not display the output in the Network Monitor UI.</span></span> <span data-ttu-id="fadd1-118">Los datos mostrados incluyen tanto los datos definidos por el analizador como los datos de la captura.</span><span class="sxs-lookup"><span data-stu-id="fadd1-118">Displayed data includes both parser-defined data, and the data in the capture.</span></span> <span data-ttu-id="fadd1-119">Por ejemplo, el analizador suele proporcionar un nombre para una propiedad que se muestra, y los datos de la captura que están asociados a la propiedad.</span><span class="sxs-lookup"><span data-stu-id="fadd1-119">For example, the parser typically provides both a name for a property that is displayed, and the data in the capture that is associated with the property.</span></span>



| <span data-ttu-id="fadd1-120">Para información acerca de</span><span class="sxs-lookup"><span data-stu-id="fadd1-120">For information about</span></span>                                         | <span data-ttu-id="fadd1-121">Vea</span><span class="sxs-lookup"><span data-stu-id="fadd1-121">See</span></span>                                                                    |
|---------------------------------------------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="fadd1-122">Qué puntos de entrada se deben implementar en el archivo DLL del analizador.</span><span class="sxs-lookup"><span data-stu-id="fadd1-122">Which entry points must be implemented within the parser DLL.</span></span> | [<span data-ttu-id="fadd1-123">Arquitectura de DLL de analizador</span><span class="sxs-lookup"><span data-stu-id="fadd1-123">Parser DLL Architecture</span></span>](parser-dll-architecture.md)                 |
| <span data-ttu-id="fadd1-124">Cómo implementar funciones de exportación de DLL de analizador.</span><span class="sxs-lookup"><span data-stu-id="fadd1-124">How to implement parser DLL export functions.</span></span>                 | [<span data-ttu-id="fadd1-125">Escritura de un analizador de protocolos</span><span class="sxs-lookup"><span data-stu-id="fadd1-125">Writing a Protocol Parser</span></span>](writing-a-protocol-parser.md)             |
| <span data-ttu-id="fadd1-126">Qué funciones y estructuras usan los analizadores.</span><span class="sxs-lookup"><span data-stu-id="fadd1-126">Which functions and structures parsers use.</span></span>                   | [<span data-ttu-id="fadd1-127">Funciones y estructuras del analizador</span><span class="sxs-lookup"><span data-stu-id="fadd1-127">Parser Functions and Structures</span></span>](parser-functions-and-structures.md) |



 

 

 



