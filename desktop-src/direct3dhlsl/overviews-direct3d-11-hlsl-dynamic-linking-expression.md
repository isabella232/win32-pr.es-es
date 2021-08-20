---
title: Restricciones de uso de la interfaz
description: El hardware de GPU actual no admite distinta información de ranura en tiempo de ejecución del sombreador. Como consecuencia, las referencias de interfaz no se pueden modificar dentro de una expresión condicional, como una instrucción if o switch.
ms.assetid: 95a505d8-3ec4-49b7-bb2b-f29a655e4225
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: eae44bbdb93ab2b3ffa0d09385c56b463192cc68c17e0454f9edd3326f722d29
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119672565"
---
# <a name="interface-usage-restrictions"></a>Restricciones de uso de la interfaz

El hardware de GPU actual no admite distinta información de ranura en tiempo de ejecución del sombreador. Como consecuencia, las referencias de interfaz no se pueden modificar dentro de una expresión condicional, como una instrucción if o switch.

El siguiente código de sombreador muestra cuándo se producirá esta restricción y un posible enfoque alternativo.

Dadas las siguientes declaraciones de interfaz:


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



Dadas las siguientes declaraciones de clase:


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



No se puede modificar una referencia de interfaz dentro de la expresión condicional (una instrucción if):


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



Dadas las mismas declaraciones de interfaz y clase, podría usar un índice para proporcionar la misma funcionalidad y evitar la inscripción forzada del bucle.


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



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Vinculación dinámica](overviews-direct3d-11-hlsl-dynamic-linking.md)
</dt> </dl>

 

 




