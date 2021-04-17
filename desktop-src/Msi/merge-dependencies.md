---
description: La propiedad dependencias de solo lectura del objeto Merge devuelve una colección de objetos de dependencia que enumera un conjunto de dependencias incorrectas para la base de datos actual.
ms.assetid: d7081ffe-3d9e-486e-84b6-b45e92fff5f0
title: Propiedad Merge. dependencies (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.Dependencies
- IMsmMerge.get_Dependencies
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 4c92d24ac2172b0d14de8e0609a407f2a0808494
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653602"
---
# <a name="mergedependencies-property"></a><span data-ttu-id="1d2c2-103">Merge. dependencies (propiedad)</span><span class="sxs-lookup"><span data-stu-id="1d2c2-103">Merge.Dependencies property</span></span>

<span data-ttu-id="1d2c2-104">La propiedad **dependencias** de solo lectura del objeto [**Merge**](merge-object.md) devuelve una colección de objetos de [**dependencia**](dependency-object.md) que enumera un conjunto de dependencias incorrectas para la base de datos actual.</span><span class="sxs-lookup"><span data-stu-id="1d2c2-104">The read-only **Dependencies** property of the [**Merge**](merge-object.md) object returns a collection of [**Dependency**](dependency-object.md) objects that enumerates a set of unsatisfied dependencies for the current database.</span></span>

<span data-ttu-id="1d2c2-105">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="1d2c2-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d2c2-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1d2c2-106">Syntax</span></span>


```JScript
propVal = Merge.Dependencies
```



## <a name="property-value"></a><span data-ttu-id="1d2c2-107">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="1d2c2-107">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="1d2c2-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1d2c2-108">Remarks</span></span>

<span data-ttu-id="1d2c2-109">No es necesario que un módulo esté abierto para recuperar la información de dependencia.</span><span class="sxs-lookup"><span data-stu-id="1d2c2-109">A module does not need to be open to retrieve dependency information.</span></span>

### <a name="c"></a><span data-ttu-id="1d2c2-110">C++</span><span class="sxs-lookup"><span data-stu-id="1d2c2-110">C++</span></span>

<span data-ttu-id="1d2c2-111">Vea la función [**Get \_ dependencies**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-get_dependencies) .</span><span class="sxs-lookup"><span data-stu-id="1d2c2-111">See [**get\_Dependencies**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-get_dependencies) Function.</span></span>

## <a name="requirements"></a><span data-ttu-id="1d2c2-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1d2c2-112">Requirements</span></span>



| <span data-ttu-id="1d2c2-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="1d2c2-113">Requirement</span></span> | <span data-ttu-id="1d2c2-114">Value</span><span class="sxs-lookup"><span data-stu-id="1d2c2-114">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1d2c2-115">Versión</span><span class="sxs-lookup"><span data-stu-id="1d2c2-115">Version</span></span><br/> | <span data-ttu-id="1d2c2-116">Mergemod.dll 1,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="1d2c2-116">Mergemod.dll 1.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="1d2c2-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1d2c2-117">Header</span></span><br/>  | <dl> <span data-ttu-id="1d2c2-118"><dt>Mergemod. h</dt></span><span class="sxs-lookup"><span data-stu-id="1d2c2-118"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="1d2c2-119">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="1d2c2-119">DLL</span></span><br/>     | <dl> <span data-ttu-id="1d2c2-120"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1d2c2-120"><dt>Mergemod.dll</dt></span></span> </dl> |



 

 
