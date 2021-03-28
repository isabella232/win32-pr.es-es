---
title: Restricciones de uso de la interfaz
description: El hardware de la GPU actual no admite la información de ranura variable en tiempo de ejecución del sombreador. Como consecuencia, las referencias a la interfaz de consecuencia no se pueden modificar en una expresión condicional como una instrucción if o switch.
ms.assetid: 95a505d8-3ec4-49b7-bb2b-f29a655e4225
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8825d192dcb874ce8b148c4ade5c579a55857311
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104356944"
---
# <a name="interface-usage-restrictions"></a><span data-ttu-id="a7e9d-104">Restricciones de uso de la interfaz</span><span class="sxs-lookup"><span data-stu-id="a7e9d-104">Interface Usage Restrictions</span></span>

<span data-ttu-id="a7e9d-105">El hardware de la GPU actual no admite la información de ranura variable en tiempo de ejecución del sombreador.</span><span class="sxs-lookup"><span data-stu-id="a7e9d-105">Current GPU hardware does not support varying slot information at shader runtime.</span></span> <span data-ttu-id="a7e9d-106">Como consecuencia, las referencias a la interfaz de consecuencia no se pueden modificar en una expresión condicional como una instrucción if o switch.</span><span class="sxs-lookup"><span data-stu-id="a7e9d-106">As a consequence interface references cannot be modified within a conditional expression such as an if or switch statement.</span></span>

<span data-ttu-id="a7e9d-107">El código del sombreador siguiente muestra Cuándo se producirá esta restricción y un posible enfoque alternativo.</span><span class="sxs-lookup"><span data-stu-id="a7e9d-107">The following shader code illustrates when this restriction will occur and a possible alternate approach.</span></span>

<span data-ttu-id="a7e9d-108">Dadas las siguientes declaraciones de interfaz:</span><span class="sxs-lookup"><span data-stu-id="a7e9d-108">Given the following interface declarations:</span></span>


```
interface A
{
    float GetRatio();
    bool IsGood();
};

interface B
{
    float GetValue();
};

A arrayA[6];
B arrayB[6];
```



<span data-ttu-id="a7e9d-109">Dadas las declaraciones de clase siguientes:</span><span class="sxs-lookup"><span data-stu-id="a7e9d-109">Given the following class declarations:</span></span>


```
class C1 : A
{
    float var;
    float GetRatio() { return 1.0f; }
    bool IsGood() { return true; }
};

class C2 : C1, B
{
    float GetRatio() { return C1::GetRatio() * 0.33f; }
    float GetValue() { return 5.0f; }
    bool IsGood() { return false; }
};

class C3 : B
{
    float var;
    float GetValue() { return -1.0f; }
};

class C4 : A, B
{
    float var;
    float GetRatio() { return var; }
    float GetValue() { return var * 2.0f; }
    bool IsGood() { return var > 0.0f; }
};
```



<span data-ttu-id="a7e9d-110">Una referencia de interfaz no se puede modificar dentro de la expresión condicional (instrucción If):</span><span class="sxs-lookup"><span data-stu-id="a7e9d-110">An interface reference cannot be modified within the conditional expression (an if statement):</span></span>


```
float main() : wicked
{
    float rev;
    {
        A a = arrayA[0];
        for( uint i = 0; i < 6; ++i )
        {
            if( arrayA[i].IsGood() )
            {
                // This forces the loop to be unrolled, 
                // since the slot information is changing.
                a = arrayA[i]; 
                rev -= arrayA[i-2].GetRatio();
            }
            else
            {
                // This causes an error since the compiler is
                // unable to determine the interface slot
                rev += arrayB[i].GetValue() + a.GetRatio(); 
            }
        }
    }
    return rev;
}
```



<span data-ttu-id="a7e9d-111">Dadas las mismas declaraciones de interfaz y clase, podría usar un índice para proporcionar la misma funcionalidad y evitar el deshacer el bucle forzado.</span><span class="sxs-lookup"><span data-stu-id="a7e9d-111">Given the same interface and class declarations, you could use an index to provide the same functionality and avoid the forced loop unroll.</span></span>


```
float main() : wicked
{
    float rev;
    {
        uint index = 0;
        for( uint i = 0; i < 6; ++i )
        {
            if( arrayA[i].IsGood() )
            {
                index = i;
                rev -= arrayA[i-2].GetRatio();
            }
            else
            {
                rev += arrayB[i].GetValue() + arrayA[index].GetRatio();
            }
        }
    }
    return rev;
}
```



## <a name="related-topics"></a><span data-ttu-id="a7e9d-112">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a7e9d-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a7e9d-113">Vinculación dinámica</span><span class="sxs-lookup"><span data-stu-id="a7e9d-113">Dynamic Linking</span></span>](overviews-direct3d-11-hlsl-dynamic-linking.md)
</dt> </dl>

 

 




