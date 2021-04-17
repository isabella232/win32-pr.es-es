---
description: La propiedad DatabaseKeys de solo lectura del objeto error devuelve una colección de cadenas que contiene las claves principales de la fila de la base de datos que produce el error. Hay una clave por cada entrada de la colección.
ms.assetid: 416a6cef-4c70-4c06-a8d2-801c9440e25a
title: Propiedad error. DatabaseKeys (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Error.DatabaseKeys
- IMsmError.get_DatabaseKeys
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: c0de387c0101e7b79e64486089abcbd49f5d60d9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653308"
---
# <a name="errordatabasekeys-property"></a><span data-ttu-id="b5515-104">Error. DatabaseKeys (propiedad)</span><span class="sxs-lookup"><span data-stu-id="b5515-104">Error.DatabaseKeys property</span></span>

<span data-ttu-id="b5515-105">La propiedad **DatabaseKeys** de solo lectura del objeto [**error**](error-object.md) devuelve una colección de cadenas que contiene las claves principales de la fila de la base de datos que produce el error.</span><span class="sxs-lookup"><span data-stu-id="b5515-105">The read-only **DatabaseKeys** property of the [**Error**](error-object.md) object returns a string collection that contains the primary keys of the database row causing the error.</span></span> <span data-ttu-id="b5515-106">Hay una clave por cada entrada de la colección.</span><span class="sxs-lookup"><span data-stu-id="b5515-106">There is one key per entry in the collection.</span></span>

<span data-ttu-id="b5515-107">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="b5515-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5515-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b5515-108">Syntax</span></span>


```JScript
propVal = Error.DatabaseKeys
```



## <a name="property-value"></a><span data-ttu-id="b5515-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="b5515-109">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="b5515-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b5515-110">Remarks</span></span>

<span data-ttu-id="b5515-111">El cliente es responsable de liberar la colección de cadenas cuando ya no se necesita.</span><span class="sxs-lookup"><span data-stu-id="b5515-111">The client is responsible for releasing the string collection when it is no longer needed.</span></span>

<span data-ttu-id="b5515-112">La colección está vacía si los valores no se aplican al tipo del error.</span><span class="sxs-lookup"><span data-stu-id="b5515-112">The collection is empty if the values do not apply to the type of the error.</span></span> <span data-ttu-id="b5515-113">Puede determinar el tipo de error llamando a la propiedad [**Type**](error-type.md) del objeto [**error**](error-object.md) .</span><span class="sxs-lookup"><span data-stu-id="b5515-113">You can determine the type of error by calling the [**Type**](error-type.md) property of the [**Error**](error-object.md) object.</span></span>

### <a name="c"></a><span data-ttu-id="b5515-114">C++</span><span class="sxs-lookup"><span data-stu-id="b5515-114">C++</span></span>

<span data-ttu-id="b5515-115">Consulte [**Get \_ DatabaseKeys**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_databasekeys) function.</span><span class="sxs-lookup"><span data-stu-id="b5515-115">See [**get\_DatabaseKeys**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_databasekeys) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="b5515-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b5515-116">Requirements</span></span>



| <span data-ttu-id="b5515-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="b5515-117">Requirement</span></span> | <span data-ttu-id="b5515-118">Value</span><span class="sxs-lookup"><span data-stu-id="b5515-118">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b5515-119">Versión</span><span class="sxs-lookup"><span data-stu-id="b5515-119">Version</span></span><br/> | <span data-ttu-id="b5515-120">Mergemod.dll 1,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="b5515-120">Mergemod.dll 1.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="b5515-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b5515-121">Header</span></span><br/>  | <dl> <span data-ttu-id="b5515-122"><dt>Mergemod. h</dt></span><span class="sxs-lookup"><span data-stu-id="b5515-122"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="b5515-123">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b5515-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="b5515-124"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b5515-124"><dt>Mergemod.dll</dt></span></span> </dl> |



 

