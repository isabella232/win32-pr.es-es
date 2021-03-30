---
description: Una anotación es una parte de la información definida por el usuario, declarada con la sintaxis siguiente.
ms.assetid: 9178e61e-05a4-441c-a9f1-e05e23ab48a5
title: Sintaxis de anotación (Direct3D 10)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 303065e9c49c380a5accba6faadbc641ec0f528a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907549"
---
# <a name="annotation-syntax-direct3d-10"></a><span data-ttu-id="0f053-103">Sintaxis de anotación (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="0f053-103">Annotation Syntax (Direct3D 10)</span></span>

<span data-ttu-id="0f053-104">Una anotación es una parte de la información definida por el usuario, declarada con la sintaxis siguiente.</span><span class="sxs-lookup"><span data-stu-id="0f053-104">An annotation is a user-defined piece of information, declared with the following syntax.</span></span>



| <span data-ttu-id="0f053-105"><Valor del nombre *DataType*   =  ;...; ></span><span class="sxs-lookup"><span data-stu-id="0f053-105"><*DataType* *Name* = *Value*; ... ;></span></span> |
|--------------------------------------------|



 

## <a name="parameters"></a><span data-ttu-id="0f053-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0f053-106">Parameters</span></span>



| <span data-ttu-id="0f053-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="0f053-107">Item</span></span>                                                                                                   | <span data-ttu-id="0f053-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="0f053-108">Description</span></span>                                                                                                                                                                      |
|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f053-109"><span id="DataType"></span><span id="datatype"></span><span id="DATATYPE"></span>*Tipo*</span><span class="sxs-lookup"><span data-stu-id="0f053-109"><span id="DataType"></span><span id="datatype"></span><span id="DATATYPE"></span>*DataType*</span></span><br/> | <span data-ttu-id="0f053-110">\[en \] el tipo de datos, que incluye cualquier tipo de [HLSL escalar](../direct3dhlsl/dx-graphics-hlsl-scalar.md) , así como el [tipo de cadena](../direct3dhlsl/dx-graphics-hlsl-scalar.md).</span><span class="sxs-lookup"><span data-stu-id="0f053-110">\[in\] The data type, which includes any [scalar HLSL](../direct3dhlsl/dx-graphics-hlsl-scalar.md) type as well as the [string type](../direct3dhlsl/dx-graphics-hlsl-scalar.md).</span></span><br/> |
| <span data-ttu-id="0f053-111"><span id="Name"></span><span id="name"></span><span id="NAME"></span>*Name*</span><span class="sxs-lookup"><span data-stu-id="0f053-111"><span id="Name"></span><span id="name"></span><span id="NAME"></span>*Name*</span></span><br/>                 | <span data-ttu-id="0f053-112">\[en \] una cadena ASCII, que representa el nombre de la anotación.</span><span class="sxs-lookup"><span data-stu-id="0f053-112">\[in\] An ASCII string, that represents the annotation name.</span></span><br/>                                                                                                          |
| <span data-ttu-id="0f053-113"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>*Valor*</span><span class="sxs-lookup"><span data-stu-id="0f053-113"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>*Value*</span></span><br/>             | <span data-ttu-id="0f053-114">\[en \] el valor inicial de la anotación.</span><span class="sxs-lookup"><span data-stu-id="0f053-114">\[in\] The initial value of the annotation.</span></span><br/>                                                                                                                           |
| <span data-ttu-id="0f053-115"><span id="..."></span>*...*</span><span class="sxs-lookup"><span data-stu-id="0f053-115"><span id="..."></span>*...*</span></span><br/>                                                                 | <span data-ttu-id="0f053-116">\[en \] anotaciones adicionales (pares nombre-valor).</span><span class="sxs-lookup"><span data-stu-id="0f053-116">\[in\] Additional annotations (name-value pairs).</span></span><br/>                                                                                                                     |



 

## <a name="remarks"></a><span data-ttu-id="0f053-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0f053-117">Remarks</span></span>

<span data-ttu-id="0f053-118">Puede agregar más de una anotación dentro de los corchetes angulares, cada una separada por un punto y coma.</span><span class="sxs-lookup"><span data-stu-id="0f053-118">You may add more than one annotation within the angle brackets, each one separated by a semicolon.</span></span> <span data-ttu-id="0f053-119">Las API del marco de efecto reconocen las anotaciones en las variables globales; se omiten todas las demás anotaciones.</span><span class="sxs-lookup"><span data-stu-id="0f053-119">The effect framework APIs recognize annotations on global variables; all other annotations are ignored.</span></span>

## <a name="example"></a><span data-ttu-id="0f053-120">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="0f053-120">Example</span></span>

<span data-ttu-id="0f053-121">Estos son algunos ejemplos.</span><span class="sxs-lookup"><span data-stu-id="0f053-121">Here are some examples.</span></span>


```
       
int i <int blabla=27; string blacksheep="Hello There";>;

int j <int bambam=30; string blacksheep="Goodbye There";> = 5 ;

float y <float y=2.3;> = 2.3, z <float y=1.3;> = 1.3 ;

half w <half GlobalW = 3.62;>;

float4 main(float4 pos : SV_POSITION ) : SV_POSITION
{
    pos.y = pos.x > 0 ? pos.w * 1.3 : pos.z * .032;
    for (int x = i; x < j ; x++) 
    {
        pos.w = pos.w * pos.y + x + j - y * w;
    } 

return pos;
}
```



## <a name="related-topics"></a><span data-ttu-id="0f053-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0f053-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0f053-123">Sintaxis de variables de efectos</span><span class="sxs-lookup"><span data-stu-id="0f053-123">Effect Variable Syntax</span></span>](d3d10-effect-variable-syntax.md)
</dt> </dl>

 

 
