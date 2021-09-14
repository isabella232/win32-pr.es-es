---
title: Reglas de empaquetado para variables constantes
description: Las reglas de empaquetado determinan la forma en que se pueden organizar los datos de forma estricta cuando se almacenan.
ms.assetid: 5c399342-06e1-47d2-8ecf-e093ed04be50
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d85566083dc9ead93a1a9e73fb06051b62178114
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127258460"
---
# <a name="packing-rules-for-constant-variables"></a>Reglas de empaquetado para variables constantes

Las reglas de empaquetado determinan la forma en que se pueden organizar los datos de forma estricta cuando se almacenan. HLSL implementa reglas de empaquetado para los datos de salida de VS, los datos de entrada y salida de GS y los datos de entrada y salida de PS. (Los datos no se empaquetan para las entradas de VS porque la fase IA no puede desempaquetar datos).

Las reglas de empaquetado HLSL son similares a la realización de un **\# paquete pragma 4** con Visual Studio, que empaqueta los datos en límites de 4 bytes. Además, HLSL empaqueta datos para que no crucen un límite de 16 bytes. Las variables se empaquetan en un vector de cuatro componentes determinado hasta que la variable se delimitará por un límite de 4 vectores. Las siguientes variables se saltarán al siguiente vector de cuatro componentes.

Cada estructura fuerza a la siguiente variable a iniciarse en el siguiente vector de cuatro componentes. Esto a veces genera relleno para matrices de estructuras. El tamaño resultante de cualquier estructura siempre será divisible uniformemente por **sizeof**(*vector de cuatro componentes*).

Las matrices no se empaquetan en HLSL de forma predeterminada. Para evitar forzar al sombreador a asumir la sobrecarga de ALU para los cálculos de desplazamiento, todos los elementos de una matriz se almacenan en un vector de cuatro componentes. Tenga en cuenta que puede lograr el empaquetado de matrices (e incurrir en los cálculos de direccionamiento) mediante la conversión.

A continuación se muestran ejemplos de estructuras y sus tamaños empaquetados correspondientes (dado: **float1** ocupa 4 bytes):


```
//  2 x 16byte elements
cbuffer IE
{
    float4 Val1;
    float2 Val2;  // starts a new vector
    float2 Val3;
};

//  3 x 16byte elements
cbuffer IE
{
    float2 Val1;
    float4 Val2;  // starts a new vector
    float2 Val3;  // starts a new vector
};

//  1 x 16byte elements
cbuffer IE
{
    float1 Val1;
    float1 Val2;
    float2 Val3;
};

//  1 x 16byte elements
cbuffer IE
{
    float1 Val1;
    float2 Val2;
    float1 Val3;
};

//  2 x 16byte elements
cbuffer IE
{
    float1 Val1;
    float1 Val1;
    float1 Val1;
    float2 Val2;    // starts a new vector
};


//  1 x 16byte elements
cbuffer IE
{
    float3 Val1;
    float1 Val2;
};

//  1 x 16byte elements
cbuffer IE
{
    float1 Val1;
    float3 Val2;
};

//  2 x 16byte elements
cbuffer IE
{
    float1 Val1;
    float1 Val1;
    float3 Val2;        // starts a new vector
};


// 3 x 16byte elements
cbuffer IE
{
    float1 Val1;

    struct     {
        float4 SVal1;    // starts a new vector
        float1 SVal2;    // starts a new vector
    } Val2;
};

// 3 x 16byte elements
cbuffer IE
{
    float1 Val1;  
    struct     {
        float1 SVal1;     // starts a new vector
        float4 SVal2;     // starts a new vector
    } Val2;
};

// 3 x 16byte elements
cbuffer IE
{
    struct     {
        float4 SVal1;
        float1 SVal2;    // starts a new vector
    } Val1;

    float1 Val2; 
};
```



## <a name="more-aggressive-packing"></a>Empaquetado más agresivo

Podría empaquetar una matriz de forma más agresiva. Por ejemplo, dada una matriz de variables float:


```
float4 array[16];
```



Puede optar por empaquetar de esta manera, sin espacios en la matriz:


```
static float2 aggressivePackArray[32] = (float2[32])array;  
```



El empaquetado más estricto es un ajuste frente a la necesidad de instrucciones adicionales del sombreador para el cálculo de direcciones.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Shader Model 4](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

 




