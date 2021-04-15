---
description: La arquitectura de la DLL del analizador debe proporcionar las características que se muestran en la siguiente ilustración.
ms.assetid: 2da5d4bc-a219-47b5-8522-1237f7bcac16
title: Arquitectura de DLL de analizador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7852029a892d8b74c954cbc2d7341fcaf29032fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104498143"
---
# <a name="parser-dll-architecture"></a><span data-ttu-id="93ae2-103">Arquitectura de DLL de analizador</span><span class="sxs-lookup"><span data-stu-id="93ae2-103">Parser DLL Architecture</span></span>

<span data-ttu-id="93ae2-104">La arquitectura de la DLL del analizador debe proporcionar las características que se muestran en la siguiente ilustración.</span><span class="sxs-lookup"><span data-stu-id="93ae2-104">The architecture of the parser DLL must provide the features shown in the following illustration.</span></span> <span data-ttu-id="93ae2-105">Tenga en cuenta que algunas características requieren la implementación de un solo punto de entrada.</span><span class="sxs-lookup"><span data-stu-id="93ae2-105">Be aware that some features require the implementation of only one entry point.</span></span> <span data-ttu-id="93ae2-106">Sin embargo, si el archivo DLL del analizador admite varios protocolos, la característica requiere la implementación de varios puntos de entrada.</span><span class="sxs-lookup"><span data-stu-id="93ae2-106">However, if your parser DLL supports multiple protocols, then the feature requires the implementation of multiple entry points.</span></span>

![características de dll de analizador](images/parserarchitecture1.png)



| <span data-ttu-id="93ae2-108">Para información acerca de</span><span class="sxs-lookup"><span data-stu-id="93ae2-108">For information about</span></span>                                                  | <span data-ttu-id="93ae2-109">Vea</span><span class="sxs-lookup"><span data-stu-id="93ae2-109">See</span></span>                                                                    |
|------------------------------------------------------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="93ae2-110">Cómo implementar funciones de exportación de DLL de analizador.</span><span class="sxs-lookup"><span data-stu-id="93ae2-110">How to implement parser DLL export functions.</span></span>                          | [<span data-ttu-id="93ae2-111">Escritura de un analizador de protocolos</span><span class="sxs-lookup"><span data-stu-id="93ae2-111">Writing a Protocol Parser</span></span>](writing-a-protocol-parser.md)             |
| <span data-ttu-id="93ae2-112">Funciones y estructuras específicas que los analizadores usan: temas de referencia.</span><span class="sxs-lookup"><span data-stu-id="93ae2-112">Specific functions and structures that parsers use — reference topics.</span></span> | [<span data-ttu-id="93ae2-113">Funciones y estructuras del analizador</span><span class="sxs-lookup"><span data-stu-id="93ae2-113">Parser Functions and Structures</span></span>](parser-functions-and-structures.md) |



 

 

 



