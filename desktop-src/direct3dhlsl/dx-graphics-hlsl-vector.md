---
title: Tipo de vector (HLSL)
description: Un vector contiene entre uno y cuatro componentes escalares; cada componente de un vector debe ser del mismo tipo.
ms.assetid: 16e66f3c-c513-4d03-8adf-463dc8d83e12
keywords:
- Tipo de vector HLSL
topic_type:
- apiref
api_name:
- Vector Type
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 76d07da5d22dfb44215f70a7620d6519b5c8a802
ms.sourcegitcommit: 3d9dce1bd6c84e2b51759e940aa95aa9b459cd20
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/04/2021
ms.locfileid: "104997997"
---
# <a name="vector-type"></a><span data-ttu-id="cdea0-104">Tipo de vector</span><span class="sxs-lookup"><span data-stu-id="cdea0-104">Vector Type</span></span>

<span data-ttu-id="cdea0-105">Un vector contiene entre uno y cuatro componentes escalares; cada componente de un vector debe ser del mismo tipo.</span><span class="sxs-lookup"><span data-stu-id="cdea0-105">A vector contains between one and four scalar components; every component of a vector must be of the same type.</span></span>



|                     |
|---------------------|
| <span data-ttu-id="cdea0-106">**Nombre de TypeNumber**</span><span class="sxs-lookup"><span data-stu-id="cdea0-106">**TypeNumber Name**</span></span> |



 


```
TypeComponents Name
```



## <a name="components"></a><span data-ttu-id="cdea0-107">Componentes</span><span class="sxs-lookup"><span data-stu-id="cdea0-107">Components</span></span>



| <span data-ttu-id="cdea0-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="cdea0-108">Item</span></span>                                                                                                                             | <span data-ttu-id="cdea0-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="cdea0-109">Description</span></span>                                                                                                                                                                                                           |
|----------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cdea0-110"><span id="TypeComponents"></span><span id="typecomponents"></span><span id="TYPECOMPONENTS"></span>**TypeComponents**</span><span class="sxs-lookup"><span data-stu-id="cdea0-110"><span id="TypeComponents"></span><span id="typecomponents"></span><span id="TYPECOMPONENTS"></span>**TypeComponents**</span></span><br/> | <span data-ttu-id="cdea0-111">Un nombre único que contiene dos partes.</span><span class="sxs-lookup"><span data-stu-id="cdea0-111">A single name that contains two parts.</span></span> <span data-ttu-id="cdea0-112">La primera parte es uno de los tipos [escalares](dx-graphics-hlsl-data-types.md) .</span><span class="sxs-lookup"><span data-stu-id="cdea0-112">The first part is one of the [scalar](dx-graphics-hlsl-data-types.md) types.</span></span> <span data-ttu-id="cdea0-113">La segunda parte es el número de componentes, que debe estar entre 1 y 4, ambos incluidos.</span><span class="sxs-lookup"><span data-stu-id="cdea0-113">The second part is the number of components, which must be between 1 and 4 inclusive.</span></span><br/> |
| <span data-ttu-id="cdea0-114"><span id="Name"></span><span id="name"></span><span id="NAME"></span>**Name**</span><span class="sxs-lookup"><span data-stu-id="cdea0-114"><span id="Name"></span><span id="name"></span><span id="NAME"></span>**Name**</span></span><br/>                                         | <span data-ttu-id="cdea0-115">Cadena ASCII que identifica de forma única el nombre de la variable.</span><span class="sxs-lookup"><span data-stu-id="cdea0-115">An ASCII string that uniquely identifies the variable name.</span></span><br/>                                                                                                                                                |



 

## <a name="examples"></a><span data-ttu-id="cdea0-116">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="cdea0-116">Examples</span></span>

<span data-ttu-id="cdea0-117">A continuación se muestran algunos ejemplos:</span><span class="sxs-lookup"><span data-stu-id="cdea0-117">Here are some examples:</span></span>


```
bool    bVector;   // scalar containing 1 Boolean
int1    iVector = 1;
float3  fVector = { 0.2f, 0.3f, 0.4f };
```



<span data-ttu-id="cdea0-118">Un vector se puede declarar con esta sintaxis también:</span><span class="sxs-lookup"><span data-stu-id="cdea0-118">A vector can be declared using this syntax also:</span></span>


```
vector <Type, Number> VariableName
```



<span data-ttu-id="cdea0-119">A continuación se muestran algunos ejemplos:</span><span class="sxs-lookup"><span data-stu-id="cdea0-119">Here are some examples:</span></span>


```
vector <int,    1> iVector = 1;
vector <double, 4> dVector = { 0.2, 0.3, 0.4, 0.5 };
```

## <a name="see-also"></a><span data-ttu-id="cdea0-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="cdea0-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cdea0-121">Tipos de datos (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="cdea0-121">Data Types (DirectX HLSL)</span></span>](dx-graphics-hlsl-data-types.md)
</dt> </dl>

 

 





