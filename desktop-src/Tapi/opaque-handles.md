---
description: Algunos tipos definidos por TSPI son controladores opacos.
ms.assetid: e52ed691-0479-48da-9e06-c6a0d7a20e10
title: Manipuladores opacos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2df2e0b0f608b9cefc8f0f4f538bffd452a8aab6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542822"
---
# <a name="opaque-handles"></a><span data-ttu-id="ab7dd-103">Manipuladores opacos</span><span class="sxs-lookup"><span data-stu-id="ab7dd-103">Opaque Handles</span></span>

<span data-ttu-id="ab7dd-104">Algunos tipos definidos por TSPI son controladores opacos.</span><span class="sxs-lookup"><span data-stu-id="ab7dd-104">A few types defined by TSPI are opaque handles.</span></span> <span data-ttu-id="ab7dd-105">Se usan en TSPI como referencias públicas a las estructuras de datos privadas.</span><span class="sxs-lookup"><span data-stu-id="ab7dd-105">These are used in TSPI as public references to private data structures.</span></span> <span data-ttu-id="ab7dd-106">Esto permite la comprobación de tipos de los parámetros proporcionados a los procedimientos de interfaz y, al mismo tiempo, proporciona una medida de protección de tipos.</span><span class="sxs-lookup"><span data-stu-id="ab7dd-106">This allows type-checking of parameters supplied to the interface procedures while still giving a measure of type protection.</span></span> <span data-ttu-id="ab7dd-107">Solo el propietario de la estructura de datos privada sabe cómo interpretar el tipo opaco como una referencia a su representación de la estructura de datos.</span><span class="sxs-lookup"><span data-stu-id="ab7dd-107">Only the owner of the private data structure knows how to interpret the opaque type as a reference to its data structure representation.</span></span> <span data-ttu-id="ab7dd-108">Como ejemplo de cómo se usan los identificadores opacos, considere la posibilidad de usar un dispositivo de teléfono.</span><span class="sxs-lookup"><span data-stu-id="ab7dd-108">As an example of how opaque handles are used, consider a phone device.</span></span> <span data-ttu-id="ab7dd-109">Tanto TAPI como el proveedor de servicios suelen mantener las estructuras de datos que representan sus vistas correspondientes del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ab7dd-109">Both TAPI and the service provider typically maintain data structures representing their respective views of the device.</span></span>

<span data-ttu-id="ab7dd-110">En las estructuras de datos de teléfono típicas mantenidas por TAPI y un proveedor de servicios, cada contiene un identificador opaco para la otra estructura de datos.</span><span class="sxs-lookup"><span data-stu-id="ab7dd-110">In typical phone data structures maintained by TAPI and a service provider, each contains an opaque handle for the other data structure.</span></span> <span data-ttu-id="ab7dd-111">Se intercambiaron en un paso de inicialización temprana.</span><span class="sxs-lookup"><span data-stu-id="ab7dd-111">These were exchanged at an early initialization step.</span></span> <span data-ttu-id="ab7dd-112">Cuando TAPI llama a una función TSPI, pasa el identificador opaco para hacer referencia al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ab7dd-112">When TAPI calls a TSPI function, it passes the opaque handle to refer to the device.</span></span> <span data-ttu-id="ab7dd-113">El proveedor de servicios sabe cómo resolver esto como una referencia (flecha) a su estructura de datos.</span><span class="sxs-lookup"><span data-stu-id="ab7dd-113">The service provider knows how to resolve this as a reference (arrow) to its data structure.</span></span> <span data-ttu-id="ab7dd-114">Se produce un proceso similar cuando el proveedor de servicios llama a una función de devolución de llamada en TAPI.</span><span class="sxs-lookup"><span data-stu-id="ab7dd-114">A similar process occurs when the service provider calls a callback function in TAPI.</span></span>

 

 



