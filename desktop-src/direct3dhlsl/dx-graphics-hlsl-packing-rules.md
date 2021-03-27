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
# <a name="packing-rules-for-constant-variables"></a><span data-ttu-id="3ccee-103">Reglas de empaquetado para variables constantes</span><span class="sxs-lookup"><span data-stu-id="3ccee-103">Packing Rules for Constant Variables</span></span>

<span data-ttu-id="3ccee-104">Las reglas de empaquetado determinan la manera en que los datos se pueden organizar cuando se almacenan.</span><span class="sxs-lookup"><span data-stu-id="3ccee-104">Packing rules dictate how tightly data can be arranged when it is stored.</span></span> <span data-ttu-id="3ccee-105">HLSL implementa reglas de empaquetado para datos de salida de VS, datos de entrada y salida de GS y datos de entrada y salida de PS.</span><span class="sxs-lookup"><span data-stu-id="3ccee-105">HLSL implements packing rules for VS output data, GS input and output data, and PS input and output data.</span></span> <span data-ttu-id="3ccee-106">(Los datos no están empaquetados para entradas de VS porque la fase IA no puede desempaquetar los datos).</span><span class="sxs-lookup"><span data-stu-id="3ccee-106">(Data is not packed for VS inputs because the IA stage cannot unpack data.)</span></span>

<span data-ttu-id="3ccee-107">Las reglas de empaquetado de HLSL son similares a la ejecución de un **\# pragma Pack 4** con Visual Studio, que empaqueta los datos en límites de 4 bytes.</span><span class="sxs-lookup"><span data-stu-id="3ccee-107">HLSL packing rules are similar to performing a **\#pragma pack 4** with Visual Studio, which packs data into 4-byte boundaries.</span></span> <span data-ttu-id="3ccee-108">Además, HLSL empaqueta los datos para que no cruce un límite de 16 bytes.</span><span class="sxs-lookup"><span data-stu-id="3ccee-108">Additionally, HLSL packs data so that it does not cross a 16-byte boundary.</span></span> <span data-ttu-id="3ccee-109">Las variables se empaquetan en un vector de cuatro componentes determinado hasta que la variable va a ocupar un límite de 4 vectores; las variables siguientes se rebotarán al siguiente vector de cuatro componentes.</span><span class="sxs-lookup"><span data-stu-id="3ccee-109">Variables are packed into a given four-component vector until the variable will straddle a 4-vector boundary; the next variables will be bounced to the next four-component vector.</span></span>

<span data-ttu-id="3ccee-110">Cada estructura obliga a que la variable siguiente se inicie en el siguiente vector de cuatro componentes.</span><span class="sxs-lookup"><span data-stu-id="3ccee-110">Each structure forces the next variable to start on the next four-component vector.</span></span> <span data-ttu-id="3ccee-111">En ocasiones, esto genera relleno para las matrices de estructuras.</span><span class="sxs-lookup"><span data-stu-id="3ccee-111">This sometimes generates padding for arrays of structures.</span></span> <span data-ttu-id="3ccee-112">El tamaño resultante de cualquier estructura siempre será divisible por **sizeof**(*Vector de cuatro componentes*).</span><span class="sxs-lookup"><span data-stu-id="3ccee-112">The resulting size of any structure will always be evenly divisible by **sizeof**(*four-component vector*).</span></span>

<span data-ttu-id="3ccee-113">De forma predeterminada, las matrices no están empaquetadas en HLSL.</span><span class="sxs-lookup"><span data-stu-id="3ccee-113">Arrays are not packed in HLSL by default.</span></span> <span data-ttu-id="3ccee-114">Para evitar que el sombreador asuma la sobrecarga de ALU para los cálculos de desplazamiento, todos los elementos de una matriz se almacenan en un vector de cuatro componentes.</span><span class="sxs-lookup"><span data-stu-id="3ccee-114">To avoid forcing the shader to take on ALU overhead for offset computations, every element in an array is stored in a four-component vector.</span></span> <span data-ttu-id="3ccee-115">Tenga en cuenta que puede conseguir el empaquetado para matrices (e incurrir en los cálculos de direccionamiento) mediante la conversión.</span><span class="sxs-lookup"><span data-stu-id="3ccee-115">Note that you can achieve packing for arrays (and incur the addressing calculations) by using casting.</span></span>

<span data-ttu-id="3ccee-116">A continuación se muestran ejemplos de estructuras y sus tamaños empaquetados correspondientes (dados: un **float1** ocupa 4 bytes):</span><span class="sxs-lookup"><span data-stu-id="3ccee-116">Following are examples of structures and their corresponding packed sizes (given: a **float1** occupies 4 bytes):</span></span>


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



## <a name="more-aggressive-packing"></a><span data-ttu-id="3ccee-117">Empaquetado más agresivo</span><span class="sxs-lookup"><span data-stu-id="3ccee-117">More Aggressive Packing</span></span>

<span data-ttu-id="3ccee-118">Podría empaquetar una matriz de forma más agresiva.</span><span class="sxs-lookup"><span data-stu-id="3ccee-118">You could pack an array more aggressively.</span></span> <span data-ttu-id="3ccee-119">Por ejemplo, dada una matriz de variables float:</span><span class="sxs-lookup"><span data-stu-id="3ccee-119">For instance, given an array of float variables:</span></span>


```
float4 array[16];
```



<span data-ttu-id="3ccee-120">Podría elegir empaquetarla como esta, sin espacios en la matriz:</span><span class="sxs-lookup"><span data-stu-id="3ccee-120">You could choose to pack it like this, without any spaces in the array:</span></span>


```
static float2 aggressivePackArray[32] = (float2[32])array;  
```



<span data-ttu-id="3ccee-121">El empaquetado más estrecho es un equilibrio entre la necesidad de instrucciones adicionales del sombreador para el cálculo de direcciones.</span><span class="sxs-lookup"><span data-stu-id="3ccee-121">The tighter packing is a trade off versus the need for additional shader instructions for address computation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3ccee-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3ccee-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3ccee-123">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="3ccee-123">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

 




