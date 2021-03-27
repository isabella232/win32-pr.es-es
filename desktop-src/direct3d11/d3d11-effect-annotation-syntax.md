---
title: Sintaxis de anotación (Direct3D 11)
description: Una anotación es una parte de la información definida por el usuario, declarada con la sintaxis descrita en esta sección.
ms.assetid: a81198d2-c4d7-47b5-b3b8-2de11a9ee9a3
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9583dafd3e1fb314ae6ac9e53d609bebc74a030
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103995283"
---
# <a name="annotation-syntax-direct3d-11"></a><span data-ttu-id="8e8fb-103">Sintaxis de anotación (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="8e8fb-103">Annotation Syntax (Direct3D 11)</span></span>

<span data-ttu-id="8e8fb-104">Una anotación es una parte de la información definida por el usuario, declarada con la sintaxis descrita en esta sección.</span><span class="sxs-lookup"><span data-stu-id="8e8fb-104">An annotation is a user-defined piece of information, declared with the syntax described in this section.</span></span>



| <span data-ttu-id="8e8fb-105"><Valor del nombre *DataType*   =  ; *...* ; ></span><span class="sxs-lookup"><span data-stu-id="8e8fb-105"><*DataType* *Name* = *Value*; *...* ;></span></span> |
|----------------------------------------------|



 

## <a name="parameters"></a><span data-ttu-id="8e8fb-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8e8fb-106">Parameters</span></span>



| <span data-ttu-id="8e8fb-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="8e8fb-107">Item</span></span>                                                                                                   | <span data-ttu-id="8e8fb-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="8e8fb-108">Description</span></span>                                                                                                                                                                      |
|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8e8fb-109"><span id="DataType"></span><span id="datatype"></span><span id="DATATYPE"></span>*Tipo*</span><span class="sxs-lookup"><span data-stu-id="8e8fb-109"><span id="DataType"></span><span id="datatype"></span><span id="DATATYPE"></span>*DataType*</span></span><br/> | <span data-ttu-id="8e8fb-110">\[en \] el tipo de datos, que incluye cualquier tipo de [HLSL escalar](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-scalar) , así como el [tipo de cadena](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-scalar).</span><span class="sxs-lookup"><span data-stu-id="8e8fb-110">\[in\] The data type, which includes any [scalar HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-scalar) type as well as the [string type](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-scalar).</span></span><br/> |
| <span data-ttu-id="8e8fb-111"><span id="Name"></span><span id="name"></span><span id="NAME"></span>*Name*</span><span class="sxs-lookup"><span data-stu-id="8e8fb-111"><span id="Name"></span><span id="name"></span><span id="NAME"></span>*Name*</span></span><br/>                 | <span data-ttu-id="8e8fb-112">\[en \] una cadena ASCII, que representa el nombre de la anotación.</span><span class="sxs-lookup"><span data-stu-id="8e8fb-112">\[in\] An ASCII string, that represents the annotation name.</span></span><br/>                                                                                                          |
| <span data-ttu-id="8e8fb-113"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>*Valor*</span><span class="sxs-lookup"><span data-stu-id="8e8fb-113"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>*Value*</span></span><br/>             | <span data-ttu-id="8e8fb-114">\[en \] el valor inicial de la anotación.</span><span class="sxs-lookup"><span data-stu-id="8e8fb-114">\[in\] The initial value of the annotation.</span></span><br/>                                                                                                                           |
| <span data-ttu-id="8e8fb-115"><span id="..."></span>*...*</span><span class="sxs-lookup"><span data-stu-id="8e8fb-115"><span id="..."></span>*...*</span></span><br/>                                                                 | <span data-ttu-id="8e8fb-116">\[en \] anotaciones adicionales (pares nombre-valor).</span><span class="sxs-lookup"><span data-stu-id="8e8fb-116">\[in\] Additional annotations (name-value pairs).</span></span><br/>                                                                                                                     |



 

## <a name="remarks"></a><span data-ttu-id="8e8fb-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8e8fb-117">Remarks</span></span>

<span data-ttu-id="8e8fb-118">Puede agregar más de una anotación dentro de los corchetes angulares, cada una separada por un punto y coma.</span><span class="sxs-lookup"><span data-stu-id="8e8fb-118">You may add more than one annotation within the angle brackets, each one separated by a semicolon.</span></span> <span data-ttu-id="8e8fb-119">Las API del marco de efecto reconocen las anotaciones en las variables globales; se omiten todas las demás anotaciones.</span><span class="sxs-lookup"><span data-stu-id="8e8fb-119">The effect framework APIs recognize annotations on global variables; all other annotations are ignored.</span></span>

## <a name="example"></a><span data-ttu-id="8e8fb-120">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="8e8fb-120">Example</span></span>

<span data-ttu-id="8e8fb-121">Estos son algunos ejemplos.</span><span class="sxs-lookup"><span data-stu-id="8e8fb-121">Here are some examples.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="8e8fb-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8e8fb-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8e8fb-123">Formato de efecto</span><span class="sxs-lookup"><span data-stu-id="8e8fb-123">Effect Format</span></span>](d3d11-effect-format.md)
</dt> <dt>

[<span data-ttu-id="8e8fb-124">Sintaxis de variables de efectos</span><span class="sxs-lookup"><span data-stu-id="8e8fb-124">Effect Variable Syntax</span></span>](d3d11-effect-variable-syntax.md)
</dt> </dl>

 

