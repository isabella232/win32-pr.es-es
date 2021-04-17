---
description: Esta es la propiedad IntegerData del objeto de registro. Esta propiedad de lectura y escritura transfiere datos enteros de 32 bits dentro o fuera de un campo especificado en el registro. Si un valor de campo no se puede convertir en un entero, se devuelve msiDatabaseNullInteger.
ms.assetid: abc291cd-31ba-409f-b010-8b3a71cbdc77
title: Propiedad record. IntegerData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Record.IntegerData
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: ed816c75ab6adc98b3ac19984079d840a4a447b0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653675"
---
# <a name="recordintegerdata-property"></a><span data-ttu-id="5ad9c-105">Propiedad record. IntegerData</span><span class="sxs-lookup"><span data-stu-id="5ad9c-105">Record.IntegerData property</span></span>

<span data-ttu-id="5ad9c-106">Esta es la propiedad **IntegerData** del objeto de [**registro**](record-object.md) .</span><span class="sxs-lookup"><span data-stu-id="5ad9c-106">This is the **IntegerData** property of the [**Record**](record-object.md) object.</span></span> <span data-ttu-id="5ad9c-107">Esta propiedad de lectura y escritura transfiere datos enteros de 32 bits dentro o fuera de un campo especificado en el registro.</span><span class="sxs-lookup"><span data-stu-id="5ad9c-107">This read-write property transfers 32-bit integer data in to or out of a specified field within the record.</span></span> <span data-ttu-id="5ad9c-108">Si un valor de campo no se puede convertir en un entero, se devuelve msiDatabaseNullInteger.</span><span class="sxs-lookup"><span data-stu-id="5ad9c-108">If a field value cannot be converted to an integer, msiDatabaseNullInteger is returned.</span></span>

<span data-ttu-id="5ad9c-109">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="5ad9c-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ad9c-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5ad9c-110">Syntax</span></span>


```JScript
propVal = Record.IntegerData
Record.IntegerData = propVal 
```



## <a name="property-value"></a><span data-ttu-id="5ad9c-111">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="5ad9c-111">Property value</span></span>

<span data-ttu-id="5ad9c-112">Número de campo obligatorio del valor dentro del registro, basado en 1.</span><span class="sxs-lookup"><span data-stu-id="5ad9c-112">Required field number of the value within the record, 1-based.</span></span>

## <a name="remarks"></a><span data-ttu-id="5ad9c-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5ad9c-113">Remarks</span></span>

<span data-ttu-id="5ad9c-114">Para establecer un campo de entero de registro en null, use msiDatabaseNullInteger.</span><span class="sxs-lookup"><span data-stu-id="5ad9c-114">To set a record integer field to null, use msiDatabaseNullInteger.</span></span> <span data-ttu-id="5ad9c-115">El valor devuelto de un campo inexistente es msiDatabaseNullInteger.</span><span class="sxs-lookup"><span data-stu-id="5ad9c-115">The returned value of a nonexistent field is msiDatabaseNullInteger.</span></span> <span data-ttu-id="5ad9c-116">Si se intenta almacenar un valor en un campo que no existe, se producirá un error.</span><span class="sxs-lookup"><span data-stu-id="5ad9c-116">Attempting to store a value in a nonexistent field causes an error.</span></span>

## <a name="requirements"></a><span data-ttu-id="5ad9c-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5ad9c-117">Requirements</span></span>



| <span data-ttu-id="5ad9c-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="5ad9c-118">Requirement</span></span> | <span data-ttu-id="5ad9c-119">Value</span><span class="sxs-lookup"><span data-stu-id="5ad9c-119">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ad9c-120">Versión</span><span class="sxs-lookup"><span data-stu-id="5ad9c-120">Version</span></span><br/> | <span data-ttu-id="5ad9c-121">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="5ad9c-121">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="5ad9c-122">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="5ad9c-122">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="5ad9c-123">Windows Installer en Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="5ad9c-123">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="5ad9c-124">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5ad9c-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="5ad9c-125"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5ad9c-125"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="5ad9c-126">IID</span><span class="sxs-lookup"><span data-stu-id="5ad9c-126">IID</span></span><br/>     | <span data-ttu-id="5ad9c-127">IID \_ IRecord se define como 000C1093-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="5ad9c-127">IID\_IRecord is defined as 000C1093-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                              |



 

 




