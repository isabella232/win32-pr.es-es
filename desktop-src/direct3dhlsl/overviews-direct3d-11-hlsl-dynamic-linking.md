---
title: Vinculación dinámica
description: A veces, los desarrolladores de gráficos crean sombreadores grandes y de uso general que se pueden usar en una amplia variedad de elementos de la escena.
ms.assetid: 2f5f7852-0f0a-4fad-a412-9a0d634c73b6
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d5cd10bab8e2b4a28458cad1050847e0184ce43b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103776398"
---
# <a name="dynamic-linking"></a><span data-ttu-id="35b24-103">Vinculación dinámica</span><span class="sxs-lookup"><span data-stu-id="35b24-103">Dynamic Linking</span></span>

<span data-ttu-id="35b24-104">A veces, los desarrolladores de gráficos crean sombreadores grandes y de uso general que se pueden usar en una amplia variedad de elementos de la escena.</span><span class="sxs-lookup"><span data-stu-id="35b24-104">Graphics developers sometimes create large, general-purpose shaders that can be used by a wide variety of scene items.</span></span> <span data-ttu-id="35b24-105">En tiempo de ejecución, el sombreador ejecuta condicionalmente el código adecuado para la situación determinada.</span><span class="sxs-lookup"><span data-stu-id="35b24-105">At runtime, the shader conditionally runs code appropriate for the given situation.</span></span> <span data-ttu-id="35b24-106">Desafortunadamente, estos grandes sombreadores de uso general usan registros de uso general (GPRs) de manera ineficaz y pueden ser mucho más lentos que los más pequeños y más específicos.</span><span class="sxs-lookup"><span data-stu-id="35b24-106">Unfortunately, these large, general-purpose shaders use general-purpose registers (GPRs) inefficiently, and can be much slower than smaller, more targeted shaders.</span></span>

<span data-ttu-id="35b24-107">El modelo de sombreador 5 soluciona este problema de rendimiento al introducir la vinculación dinámica del sombreador.</span><span class="sxs-lookup"><span data-stu-id="35b24-107">Shader model 5 addresses this performance problem by introducing dynamic shader linking.</span></span> <span data-ttu-id="35b24-108">La vinculación dinámica separa los fragmentos de código del sombreador mediante el uso de interfaces y funciones virtuales y permite que la aplicación Seleccione el fragmento que se va a usar en el momento de la hora de dibujo.</span><span class="sxs-lookup"><span data-stu-id="35b24-108">Dynamic linking separates shader code fragments by using interfaces and virtual functions and allows the application to select the fragment to use at draw time.</span></span> <span data-ttu-id="35b24-109">Esto mejora el rendimiento al enlazar solo el código del sombreador necesario y no todo el sombreador de uso general grande.</span><span class="sxs-lookup"><span data-stu-id="35b24-109">This improves performance by binding only the shader code needed and not the entire large, general-purpose shader.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="35b24-110">En esta sección</span><span class="sxs-lookup"><span data-stu-id="35b24-110">In This Section</span></span>



| <span data-ttu-id="35b24-111">Elemento</span><span class="sxs-lookup"><span data-stu-id="35b24-111">Item</span></span>                                                                                                                                                                                                                                                                                                                         | <span data-ttu-id="35b24-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="35b24-112">Description</span></span>                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="35b24-113"><span id="Storing_Variables_and_Types_for_Shaders_to_Share"></span><span id="storing_variables_and_types_for_shaders_to_share"></span><span id="STORING_VARIABLES_AND_TYPES_FOR_SHADERS_TO_SHARE"></span>[Almacenar variables y tipos para los sombreadores que se van a compartir](storing-variables-and-types-for-shaders-to-share.md)</span><span class="sxs-lookup"><span data-stu-id="35b24-113"><span id="Storing_Variables_and_Types_for_Shaders_to_Share"></span><span id="storing_variables_and_types_for_shaders_to_share"></span><span id="STORING_VARIABLES_AND_TYPES_FOR_SHADERS_TO_SHARE"></span>[Storing Variables and Types for Shaders to Share](storing-variables-and-types-for-shaders-to-share.md)</span></span><br/> | <span data-ttu-id="35b24-114">Describe el objeto de vinculación de clases para almacenar variables y tipos que pueden compartir varios sombreadores.</span><span class="sxs-lookup"><span data-stu-id="35b24-114">Describes the class linkage object for storing variables and types that multiple shaders can share.</span></span><br/> |
| <span data-ttu-id="35b24-115"><span id="Interfaces_and_Classes"></span><span id="interfaces_and_classes"></span><span id="INTERFACES_AND_CLASSES"></span>[Interfaces y clases](overviews-direct3d-11-hlsl-dynamic-linking-class.md)</span><span class="sxs-lookup"><span data-stu-id="35b24-115"><span id="Interfaces_and_Classes"></span><span id="interfaces_and_classes"></span><span id="INTERFACES_AND_CLASSES"></span>[Interfaces and Classes](overviews-direct3d-11-hlsl-dynamic-linking-class.md)</span></span><br/>                                                                                                         | <span data-ttu-id="35b24-116">Describe el uso de interfaces y clases HLSL para implementar la vinculación dinámica.</span><span class="sxs-lookup"><span data-stu-id="35b24-116">Describes using HLSL interfaces and classes to implement dynamic linking.</span></span><br/>                           |
| <span data-ttu-id="35b24-117"><span id="Interface_Usage_Restrictions"></span><span id="interface_usage_restrictions"></span><span id="INTERFACE_USAGE_RESTRICTIONS"></span>[Restricciones de uso de la interfaz](overviews-direct3d-11-hlsl-dynamic-linking-expression.md)</span><span class="sxs-lookup"><span data-stu-id="35b24-117"><span id="Interface_Usage_Restrictions"></span><span id="interface_usage_restrictions"></span><span id="INTERFACE_USAGE_RESTRICTIONS"></span>[Interface Usage Restrictions](overviews-direct3d-11-hlsl-dynamic-linking-expression.md)</span></span><br/>                                                                            | <span data-ttu-id="35b24-118">Describe las restricciones en el uso de interfaces en el código del sombreador.</span><span class="sxs-lookup"><span data-stu-id="35b24-118">Describes restrictions on the use of interfaces in shader code.</span></span><br/>                                     |



 

## <a name="related-topics"></a><span data-ttu-id="35b24-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="35b24-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="35b24-120">HLSL</span><span class="sxs-lookup"><span data-stu-id="35b24-120">HLSL</span></span>](overviews-direct3d-11-hlsl.md)
</dt> </dl>

 

 





