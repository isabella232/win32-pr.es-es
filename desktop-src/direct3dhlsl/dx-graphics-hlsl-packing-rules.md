---
title: Reglas de empaquetado para variables constantes
description: Las reglas de empaquetado determinan la manera en que los datos se pueden organizar cuando se almacenan.
ms.assetid: 5c399342-06e1-47d2-8ecf-e093ed04be50
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d85566083dc9ead93a1a9e73fb06051b62178114
ms.sourcegitcommit: 004d7881dc9ff92ea394cd2331774e13b1e7f13c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/12/2020
ms.locfileid: "103789424"
---
# <a name="packing-rules-for-constant-variables"></a>Reglas de empaquetado para variables constantes

Las reglas de empaquetado determinan la manera en que los datos se pueden organizar cuando se almacenan. HLSL implementa reglas de empaquetado para datos de salida de VS, datos de entrada y salida de GS y datos de entrada y salida de PS. (Los datos no están empaquetados para entradas de VS porque la fase IA no puede desempaquetar los datos).

Las reglas de empaquetado de HLSL son similares a la ejecución de un **\# pragma Pack 4** con Visual Studio, que empaqueta los datos en límites de 4 bytes. Además, HLSL empaqueta los datos para que no cruce un límite de 16 bytes. Las variables se empaquetan en un vector de cuatro componentes determinado hasta que la variable va a ocupar un límite de 4 vectores; las variables siguientes se rebotarán al siguiente vector de cuatro componentes.

Cada estructura obliga a que la variable siguiente se inicie en el siguiente vector de cuatro componentes. En ocasiones, esto genera relleno para las matrices de estructuras. El tamaño resultante de cualquier estructura siempre será divisible por **sizeof**(*Vector de cuatro componentes*).

De forma predeterminada, las matrices no están empaquetadas en HLSL. Para evitar que el sombreador asuma la sobrecarga de ALU para los cálculos de desplazamiento, todos los elementos de una matriz se almacenan en un vector de cuatro componentes. Tenga en cuenta que puede conseguir el empaquetado para matrices (e incurrir en los cálculos de direccionamiento) mediante la conversión.

A continuación se muestran ejemplos de estructuras y sus tamaños empaquetados correspondientes (dados: un **float1** ocupa 4 bytes):


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



Podría elegir empaquetarla como esta, sin espacios en la matriz:


```
static float2 aggressivePackArray[32] = (float2[32])array;  
```



El empaquetado más estrecho es un equilibrio entre la necesidad de instrucciones adicionales del sombreador para el cálculo de direcciones.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

 




