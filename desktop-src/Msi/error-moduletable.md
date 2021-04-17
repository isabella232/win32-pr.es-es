---
description: La propiedad ModuleTable de solo lectura devuelve el nombre de la tabla en el módulo que causó el error.
ms.assetid: 390f5889-d638-4c1c-b95c-76d38c934e7c
title: Propiedad error. ModuleTable (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Error.ModuleTable
- IMsmError.get_ModuleTable
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 063898419596fc852d073bf83ce7504a7691a10e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690193"
---
# <a name="errormoduletable-property"></a><span data-ttu-id="c0cf2-103">Error. ModuleTable (propiedad)</span><span class="sxs-lookup"><span data-stu-id="c0cf2-103">Error.ModuleTable property</span></span>

<span data-ttu-id="c0cf2-104">La propiedad **ModuleTable** de solo lectura devuelve el nombre de la tabla en el módulo que causó el error.</span><span class="sxs-lookup"><span data-stu-id="c0cf2-104">The read-only **ModuleTable** Property returns the name of the table in the module that caused the error.</span></span>

<span data-ttu-id="c0cf2-105">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="c0cf2-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0cf2-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c0cf2-106">Syntax</span></span>


```JScript
propVal = Error.ModuleTable
```



## <a name="property-value"></a><span data-ttu-id="c0cf2-107">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="c0cf2-107">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="c0cf2-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c0cf2-108">Remarks</span></span>

<span data-ttu-id="c0cf2-109">La colección está vacía si los valores no se aplican al tipo del error.</span><span class="sxs-lookup"><span data-stu-id="c0cf2-109">The collection is empty if the values do not apply to the type of the error.</span></span> <span data-ttu-id="c0cf2-110">Puede determinar el tipo de error llamando a la propiedad [**Type**](error-type.md) del objeto [**error**](error-object.md) .</span><span class="sxs-lookup"><span data-stu-id="c0cf2-110">You can determine the type of error by calling the [**Type**](error-type.md) property of the [**Error**](error-object.md) object.</span></span>

### <a name="c"></a><span data-ttu-id="c0cf2-111">C++</span><span class="sxs-lookup"><span data-stu-id="c0cf2-111">C++</span></span>

<span data-ttu-id="c0cf2-112">Consulte [**Get \_ ModuleTable**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_moduletable) function.</span><span class="sxs-lookup"><span data-stu-id="c0cf2-112">See [**get\_ModuleTable**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_moduletable) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="c0cf2-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c0cf2-113">Requirements</span></span>



| <span data-ttu-id="c0cf2-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="c0cf2-114">Requirement</span></span> | <span data-ttu-id="c0cf2-115">Value</span><span class="sxs-lookup"><span data-stu-id="c0cf2-115">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c0cf2-116">Versión</span><span class="sxs-lookup"><span data-stu-id="c0cf2-116">Version</span></span><br/> | <span data-ttu-id="c0cf2-117">Mergemod.dll 1,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="c0cf2-117">Mergemod.dll 1.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="c0cf2-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c0cf2-118">Header</span></span><br/>  | <dl> <span data-ttu-id="c0cf2-119"><dt>Mergemod. h</dt></span><span class="sxs-lookup"><span data-stu-id="c0cf2-119"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="c0cf2-120">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c0cf2-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="c0cf2-121"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c0cf2-121"><dt>Mergemod.dll</dt></span></span> </dl> |



 

