---
description: La propiedad ModuleKeys de solo lectura del objeto error devuelve un puntero a una colección de cadenas que contiene las claves principales de la fila del módulo que produce el error, una clave por cada entrada de la colección.
ms.assetid: b02b609b-4682-4228-b29a-364f079e863c
title: Propiedad error. ModuleKeys (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Error.ModuleKeys
- IMsmError.get_ModuleKeys
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 53d2ac37f8864318a83c13672c081ed5dea42b0a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653474"
---
# <a name="errormodulekeys-property"></a><span data-ttu-id="2068e-103">Error. ModuleKeys (propiedad)</span><span class="sxs-lookup"><span data-stu-id="2068e-103">Error.ModuleKeys property</span></span>

<span data-ttu-id="2068e-104">La propiedad **ModuleKeys** de solo lectura del objeto [**error**](error-object.md) devuelve un puntero a una colección de cadenas que contiene las claves principales de la fila del módulo que produce el error, una clave por cada entrada de la colección.</span><span class="sxs-lookup"><span data-stu-id="2068e-104">The read-only **ModuleKeys** property of the [**Error**](error-object.md) object returns a pointer to a string collection containing the primary keys of the row in the module causing the error, one key per entry in the collection.</span></span>

<span data-ttu-id="2068e-105">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="2068e-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="2068e-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2068e-106">Syntax</span></span>


```JScript
propVal = Error.ModuleKeys
```



## <a name="property-value"></a><span data-ttu-id="2068e-107">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="2068e-107">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="2068e-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2068e-108">Remarks</span></span>

<span data-ttu-id="2068e-109">El cliente es responsable de liberar la colección de cadenas cuando ya no se necesita.</span><span class="sxs-lookup"><span data-stu-id="2068e-109">The client is responsible for releasing the string collection when it is no longer needed.</span></span>

<span data-ttu-id="2068e-110">La colección está vacía si los valores no se aplican al tipo del error.</span><span class="sxs-lookup"><span data-stu-id="2068e-110">The collection is empty if the values do not apply to the type of the error.</span></span> <span data-ttu-id="2068e-111">Puede determinar el tipo de error llamando a la propiedad [**Type**](error-type.md) del objeto [**error**](error-object.md) .</span><span class="sxs-lookup"><span data-stu-id="2068e-111">You can determine the type of error by calling the [**Type**](error-type.md) property of the [**Error**](error-object.md) object.</span></span>

### <a name="c"></a><span data-ttu-id="2068e-112">C++</span><span class="sxs-lookup"><span data-stu-id="2068e-112">C++</span></span>

<span data-ttu-id="2068e-113">Consulte [**Get \_ ModuleKeys**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_modulekeys) function.</span><span class="sxs-lookup"><span data-stu-id="2068e-113">See [**get\_ModuleKeys**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_modulekeys) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="2068e-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2068e-114">Requirements</span></span>



| <span data-ttu-id="2068e-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="2068e-115">Requirement</span></span> | <span data-ttu-id="2068e-116">Value</span><span class="sxs-lookup"><span data-stu-id="2068e-116">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2068e-117">Versión</span><span class="sxs-lookup"><span data-stu-id="2068e-117">Version</span></span><br/> | <span data-ttu-id="2068e-118">Mergemod.dll 1,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="2068e-118">Mergemod.dll 1.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="2068e-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2068e-119">Header</span></span><br/>  | <dl> <span data-ttu-id="2068e-120"><dt>Mergemod. h</dt></span><span class="sxs-lookup"><span data-stu-id="2068e-120"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="2068e-121">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2068e-121">DLL</span></span><br/>     | <dl> <span data-ttu-id="2068e-122"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2068e-122"><dt>Mergemod.dll</dt></span></span> </dl> |



 

