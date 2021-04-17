---
description: La propiedad StringData del objeto Record es una propiedad de lectura y escritura que transfiere los datos de cadena dentro o fuera de un campo especificado dentro del registro. Si se ha almacenado un entero o un objeto, se devuelve su valor de cadena.
ms.assetid: ffa163eb-41b3-47ae-b01d-39a3890990a3
title: Propiedad record. StringData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Record.StringData
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 21f72c35795696875aa55f2d5d791564c6f1fee5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670965"
---
# <a name="recordstringdata-property"></a><span data-ttu-id="d0217-104">Propiedad record. StringData</span><span class="sxs-lookup"><span data-stu-id="d0217-104">Record.StringData property</span></span>

<span data-ttu-id="d0217-105">La propiedad **StringData** del objeto [**Record**](record-object.md) es una propiedad de lectura y escritura que transfiere los datos de cadena dentro o fuera de un campo especificado dentro del registro.</span><span class="sxs-lookup"><span data-stu-id="d0217-105">The **StringData** property of the [**Record**](record-object.md) object is a read-write property that transfers string data in to or out of a specified field within the record.</span></span> <span data-ttu-id="d0217-106">Si se ha almacenado un entero o un objeto, se devuelve su valor de cadena.</span><span class="sxs-lookup"><span data-stu-id="d0217-106">If an integer or object has been stored, its string value is returned.</span></span>

<span data-ttu-id="d0217-107">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="d0217-107">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0217-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d0217-108">Syntax</span></span>


```JScript
propVal = Record.StringData
Record.StringData = propVal 
```



## <a name="property-value"></a><span data-ttu-id="d0217-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="d0217-109">Property value</span></span>

<span data-ttu-id="d0217-110">Número de campo obligatorio del valor dentro del registro, basado en 1.</span><span class="sxs-lookup"><span data-stu-id="d0217-110">Required field number of the value within the record, 1-based.</span></span>

## <a name="remarks"></a><span data-ttu-id="d0217-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d0217-111">Remarks</span></span>

<span data-ttu-id="d0217-112">El valor devuelto de un campo inexistente es una cadena vacía.</span><span class="sxs-lookup"><span data-stu-id="d0217-112">The returned value of a nonexistent field is an empty string.</span></span> <span data-ttu-id="d0217-113">Para establecer un campo de cadena de registro en null, use una variante vacía o una cadena vacía.</span><span class="sxs-lookup"><span data-stu-id="d0217-113">To set a record string field to null, use either an empty variant or an empty string.</span></span> <span data-ttu-id="d0217-114">Si se intenta almacenar un valor en un campo que no existe, se producirá un error.</span><span class="sxs-lookup"><span data-stu-id="d0217-114">Attempting to store a value in a nonexistent field causes an error.</span></span>

## <a name="requirements"></a><span data-ttu-id="d0217-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d0217-115">Requirements</span></span>



| <span data-ttu-id="d0217-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="d0217-116">Requirement</span></span> | <span data-ttu-id="d0217-117">Value</span><span class="sxs-lookup"><span data-stu-id="d0217-117">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d0217-118">Versión</span><span class="sxs-lookup"><span data-stu-id="d0217-118">Version</span></span><br/> | <span data-ttu-id="d0217-119">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="d0217-119">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="d0217-120">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="d0217-120">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="d0217-121">Windows Installer en Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="d0217-121">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="d0217-122">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d0217-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="d0217-123"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d0217-123"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="d0217-124">IID</span><span class="sxs-lookup"><span data-stu-id="d0217-124">IID</span></span><br/>     | <span data-ttu-id="d0217-125">IID \_ IRecord se define como 000C1093-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="d0217-125">IID\_IRecord is defined as 000C1093-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                              |



 

 




