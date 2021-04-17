---
description: La propiedad DatabaseTable de solo lectura del objeto error devuelve el nombre de la tabla en la base de datos que causó el error.
ms.assetid: 38ff45ca-4bd6-43f3-88ad-db4077daeb77
title: Propiedad error. DatabaseTable (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Error.DatabaseTable
- IMsmError.get_DatabaseTable
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 8d7be883597d30059f6c949a800fe9803563c2b3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653307"
---
# <a name="errordatabasetable-property"></a><span data-ttu-id="6ffd2-103">Error. DatabaseTable (propiedad)</span><span class="sxs-lookup"><span data-stu-id="6ffd2-103">Error.DatabaseTable property</span></span>

<span data-ttu-id="6ffd2-104">La propiedad **DatabaseTable** de solo lectura del objeto [**error**](error-object.md) devuelve el nombre de la tabla en la base de datos que causó el error.</span><span class="sxs-lookup"><span data-stu-id="6ffd2-104">The read-only **DatabaseTable** property of the [**Error**](error-object.md) object returns the name of the table in the database that caused the error.</span></span>

<span data-ttu-id="6ffd2-105">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="6ffd2-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ffd2-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6ffd2-106">Syntax</span></span>


```JScript
propVal = Error.DatabaseTable
```



## <a name="property-value"></a><span data-ttu-id="6ffd2-107">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="6ffd2-107">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="6ffd2-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6ffd2-108">Remarks</span></span>

<span data-ttu-id="6ffd2-109">La colección está vacía si los valores no se aplican al tipo del error.</span><span class="sxs-lookup"><span data-stu-id="6ffd2-109">The collection is empty if the values do not apply to the type of the error.</span></span> <span data-ttu-id="6ffd2-110">Puede determinar el tipo de error mediante una llamada a la propiedad [**Type**](error-type.md) del objeto [**error**](error-object.md) .</span><span class="sxs-lookup"><span data-stu-id="6ffd2-110">You can determine the type of error by calling [**Type**](error-type.md) property of the [**Error**](error-object.md) object.</span></span>

### <a name="c"></a><span data-ttu-id="6ffd2-111">C++</span><span class="sxs-lookup"><span data-stu-id="6ffd2-111">C++</span></span>

<span data-ttu-id="6ffd2-112">Consulte [**Get \_ DatabaseTable**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_databasetable) function.</span><span class="sxs-lookup"><span data-stu-id="6ffd2-112">See [**get\_DatabaseTable**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_databasetable) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="6ffd2-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6ffd2-113">Requirements</span></span>



| <span data-ttu-id="6ffd2-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="6ffd2-114">Requirement</span></span> | <span data-ttu-id="6ffd2-115">Value</span><span class="sxs-lookup"><span data-stu-id="6ffd2-115">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6ffd2-116">Versión</span><span class="sxs-lookup"><span data-stu-id="6ffd2-116">Version</span></span><br/> | <span data-ttu-id="6ffd2-117">Mergemod.dll 1,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="6ffd2-117">Mergemod.dll 1.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="6ffd2-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6ffd2-118">Header</span></span><br/>  | <dl> <span data-ttu-id="6ffd2-119"><dt>Mergemod. h</dt></span><span class="sxs-lookup"><span data-stu-id="6ffd2-119"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="6ffd2-120">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6ffd2-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="6ffd2-121"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6ffd2-121"><dt>Mergemod.dll</dt></span></span> </dl> |



 

