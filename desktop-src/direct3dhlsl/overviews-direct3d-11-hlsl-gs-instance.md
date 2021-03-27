---
title: Cómo instanciar un sombreador de geometría
description: La creación de instancias del sombreador de geometría permite que se ejecuten varias ejecuciones del mismo sombreador de geometría por primitiva.
ms.assetid: e3d8616b-7129-40e9-99fc-2852914a80b0
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7858de7d8526a9468d3ebd0a07d57777983a66db
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104996788"
---
# <a name="how-to-instance-a-geometry-shader"></a><span data-ttu-id="8bb1a-103">Cómo: instanciar un sombreador de geometría</span><span class="sxs-lookup"><span data-stu-id="8bb1a-103">How To: Instance a Geometry Shader</span></span>

<span data-ttu-id="8bb1a-104">La creación de instancias del sombreador de geometría permite que se ejecuten varias ejecuciones del mismo sombreador de geometría por primitiva.</span><span class="sxs-lookup"><span data-stu-id="8bb1a-104">Geometry shader instancing allows multiple executions of the same geometry shader to be executed per primitive.</span></span> <span data-ttu-id="8bb1a-105">Para instanciar un sombreador de geometría, agregue un atributo de instancia a la función de sombreador principal e identifique un parámetro de índice de instancia en el cuerpo de la función de sombreador.</span><span class="sxs-lookup"><span data-stu-id="8bb1a-105">To instance a geometry shader, add an instance attribute to the main shader function and identify an instance index parameter in the shader function body.</span></span>

<span data-ttu-id="8bb1a-106">Para instanciar un sombreador de geometría:</span><span class="sxs-lookup"><span data-stu-id="8bb1a-106">To Instance a Geometry Shader:</span></span>

1.  <span data-ttu-id="8bb1a-107">Agregue el [atributo de instancia](sm5-attributes-instance.md) a la función main.</span><span class="sxs-lookup"><span data-stu-id="8bb1a-107">Add the [instance attribute](sm5-attributes-instance.md) to the main function.</span></span>

    ```
    [instance(24)]
    ```

    

    <span data-ttu-id="8bb1a-108">Define el número de instancias (un máximo de 32) que se va a ejecutar para cada primitiva.</span><span class="sxs-lookup"><span data-stu-id="8bb1a-108">This defines the number of instances (a maximum of 32) to be run for each primitive.</span></span>

2.  <span data-ttu-id="8bb1a-109">Adjunte el valor del sistema [VP \_ GSInstanceID](sv-gsinstanceid.md) a una variable de la lista de parámetros de función que se puede usar para realizar el seguimiento del identificador de la instancia que se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="8bb1a-109">Attach the [SV\_GSInstanceID](sv-gsinstanceid.md) system value to a variable in the function parameter list that can be used to track the ID of the instance being executed.</span></span>
    ```
    uint InstanceID : SV_GSInstanceID
    ```

    

3.  <span data-ttu-id="8bb1a-110">Compile y cree el sombreador tal como lo haría con cualquier otro sombreador de geometría.</span><span class="sxs-lookup"><span data-stu-id="8bb1a-110">Compile and create the shader just as you would any other geometry shader.</span></span>

<span data-ttu-id="8bb1a-111">Otros detalles incluyen:</span><span class="sxs-lookup"><span data-stu-id="8bb1a-111">Other details include:</span></span>

-   <span data-ttu-id="8bb1a-112">El recuento máximo de instancias es 32.</span><span class="sxs-lookup"><span data-stu-id="8bb1a-112">The maximum instance count is 32.</span></span>
-   <span data-ttu-id="8bb1a-113">El número máximo de vértices es un recuento máximo de vértices por instancia.</span><span class="sxs-lookup"><span data-stu-id="8bb1a-113">The maximum vertex count is a per-instance maximum vertex count.</span></span>
-   <span data-ttu-id="8bb1a-114">Cada invocación de instancia (como cualquier invocación del sombreador de geometría) aumenta el recuento de invocación y genera una RestartStrip implícita ().</span><span class="sxs-lookup"><span data-stu-id="8bb1a-114">Each instance invocation (like any geometry shader invocation) increases the invocation count and generates an implicit RestartStrip().</span></span>

## <a name="related-topics"></a><span data-ttu-id="8bb1a-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8bb1a-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8bb1a-116">Características del sombreador de geometría</span><span class="sxs-lookup"><span data-stu-id="8bb1a-116">Geometry Shader Features</span></span>](overviews-direct3d-11-hlsl-gs-features.md)
</dt> </dl>

 

 




