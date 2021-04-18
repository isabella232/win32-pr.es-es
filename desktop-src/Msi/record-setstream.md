---
description: El método SetStream del objeto record copia el contenido del archivo especificado en el campo registro designado como datos de flujo. Los datos de flujo no se pueden insertar en campos temporales.
ms.assetid: feb79371-d0c4-4bb0-b539-2f431ee1051b
title: Método record. SetStream
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Record.SetStream
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 94ec3d63b3dcd75a13c2c0ff62b624b89979d641
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680760"
---
# <a name="recordsetstream-method"></a><span data-ttu-id="4ee50-104">Método record. SetStream</span><span class="sxs-lookup"><span data-stu-id="4ee50-104">Record.SetStream method</span></span>

<span data-ttu-id="4ee50-105">El método **SetStream** del objeto [**Record**](record-object.md) copia el contenido del archivo especificado en el campo registro designado como datos de flujo.</span><span class="sxs-lookup"><span data-stu-id="4ee50-105">The **SetStream** method of the [**Record**](record-object.md) object copies the content of the specified file into the designated record field as stream data.</span></span> <span data-ttu-id="4ee50-106">Los datos de flujo no se pueden insertar en campos temporales.</span><span class="sxs-lookup"><span data-stu-id="4ee50-106">Stream data cannot be inserted into temporary fields.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ee50-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4ee50-107">Syntax</span></span>


```JScript
Record.SetStream(
  field,
  filePath
)
```



## <a name="parameters"></a><span data-ttu-id="4ee50-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4ee50-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4ee50-109">*campo*</span><span class="sxs-lookup"><span data-stu-id="4ee50-109">*field*</span></span> 
</dt> <dd>

<span data-ttu-id="4ee50-110">Número de campo obligatorio del valor dentro del registro, basado en 1.</span><span class="sxs-lookup"><span data-stu-id="4ee50-110">Required field number of the value within the record, 1-based.</span></span>

</dd> <dt>

<span data-ttu-id="4ee50-111">*filePath*</span><span class="sxs-lookup"><span data-stu-id="4ee50-111">*filePath*</span></span> 
</dt> <dd>

<span data-ttu-id="4ee50-112">Ubicación del archivo que se va a copiar.</span><span class="sxs-lookup"><span data-stu-id="4ee50-112">The location of the file to copy.</span></span> <span data-ttu-id="4ee50-113">No se realiza ninguna conversión de ningún tipo.</span><span class="sxs-lookup"><span data-stu-id="4ee50-113">No translation of any type is performed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4ee50-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4ee50-114">Return value</span></span>

<span data-ttu-id="4ee50-115">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="4ee50-115">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4ee50-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4ee50-116">Remarks</span></span>

<span data-ttu-id="4ee50-117">Si se produce un error en el método, puede obtener información de error extendida mediante el método [**LastErrorRecord**](installer-lasterrorrecord.md) .</span><span class="sxs-lookup"><span data-stu-id="4ee50-117">If the method fails, you can obtain extended error information by using the [**LastErrorRecord**](installer-lasterrorrecord.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="4ee50-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4ee50-118">Requirements</span></span>



| <span data-ttu-id="4ee50-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="4ee50-119">Requirement</span></span> | <span data-ttu-id="4ee50-120">Value</span><span class="sxs-lookup"><span data-stu-id="4ee50-120">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4ee50-121">Versión</span><span class="sxs-lookup"><span data-stu-id="4ee50-121">Version</span></span><br/> | <span data-ttu-id="4ee50-122">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="4ee50-122">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="4ee50-123">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="4ee50-123">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="4ee50-124">Windows Installer en Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="4ee50-124">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="4ee50-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4ee50-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="4ee50-126"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4ee50-126"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="4ee50-127">IID</span><span class="sxs-lookup"><span data-stu-id="4ee50-127">IID</span></span><br/>     | <span data-ttu-id="4ee50-128">IID \_ IRecord se define como 000C1093-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="4ee50-128">IID\_IRecord is defined as 000C1093-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                              |



 

 




