---
description: El objeto de registro es un contenedor para almacenar y transferir un número variable de valores.
ms.assetid: e832c19f-61a6-4e42-a10a-b7bb1705af59
title: Objeto record
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Record
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: c13cb31d628525e529491af1c089555ba2ad8273
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653777"
---
# <a name="record-object"></a><span data-ttu-id="0dfe8-103">Objeto record</span><span class="sxs-lookup"><span data-stu-id="0dfe8-103">Record object</span></span>

<span data-ttu-id="0dfe8-104">El objeto de **registro** es un contenedor para almacenar y transferir un número variable de valores.</span><span class="sxs-lookup"><span data-stu-id="0dfe8-104">The **Record** object is a container for holding and transferring a variable number of values.</span></span> <span data-ttu-id="0dfe8-105">Los campos del registro se indizan numéricamente y pueden contener cadenas, enteros, objetos y valores NULL.</span><span class="sxs-lookup"><span data-stu-id="0dfe8-105">Fields within the record are numerically indexed and can contain strings, integers, objects, and null values.</span></span> <span data-ttu-id="0dfe8-106">Los campos más allá del tamaño del registro asignado se tratan como si tuvieran valores NULL de forma permanente.</span><span class="sxs-lookup"><span data-stu-id="0dfe8-106">Fields beyond the allocated record size are treated as having permanently null values.</span></span> <span data-ttu-id="0dfe8-107">El número de campo 0 está reservado.</span><span class="sxs-lookup"><span data-stu-id="0dfe8-107">Field number 0 is reserved.</span></span>

## <a name="members"></a><span data-ttu-id="0dfe8-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="0dfe8-108">Members</span></span>

<span data-ttu-id="0dfe8-109">El objeto de **registro** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="0dfe8-109">The **Record** object has these types of members:</span></span>

-   [<span data-ttu-id="0dfe8-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="0dfe8-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="0dfe8-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="0dfe8-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="0dfe8-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="0dfe8-112">Methods</span></span>

<span data-ttu-id="0dfe8-113">El objeto de **registro** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="0dfe8-113">The **Record** object has these methods.</span></span>



| <span data-ttu-id="0dfe8-114">Método</span><span class="sxs-lookup"><span data-stu-id="0dfe8-114">Method</span></span>                                  | <span data-ttu-id="0dfe8-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="0dfe8-115">Description</span></span>                                                                                          |
|:----------------------------------------|:-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0dfe8-116">**ClearData**</span><span class="sxs-lookup"><span data-stu-id="0dfe8-116">**ClearData**</span></span>](record-cleardata.md)   | <span data-ttu-id="0dfe8-117">Borra los datos de todos los campos y los establece en NULL.</span><span class="sxs-lookup"><span data-stu-id="0dfe8-117">Clears the data in all fields, setting them to null.</span></span><br/>                                      |
| [<span data-ttu-id="0dfe8-118">**FormatText**</span><span class="sxs-lookup"><span data-stu-id="0dfe8-118">**FormatText**</span></span>](record-formattext.md) | <span data-ttu-id="0dfe8-119">Da formato a los campos según la plantilla del campo 0.</span><span class="sxs-lookup"><span data-stu-id="0dfe8-119">Formats fields according to the template in field 0.</span></span><br/>                                      |
| [<span data-ttu-id="0dfe8-120">**ReadStream**</span><span class="sxs-lookup"><span data-stu-id="0dfe8-120">**ReadStream**</span></span>](record-readstream.md) | <span data-ttu-id="0dfe8-121">Lee un número especificado de bytes de un campo de registro que contiene los datos de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="0dfe8-121">Reads a specified number of bytes from a record field holding stream data.</span></span><br/>                |
| [<span data-ttu-id="0dfe8-122">**SetStream**</span><span class="sxs-lookup"><span data-stu-id="0dfe8-122">**SetStream**</span></span>](record-setstream.md)   | <span data-ttu-id="0dfe8-123">Copia el contenido del archivo especificado en el campo de registro designado como datos de flujo.</span><span class="sxs-lookup"><span data-stu-id="0dfe8-123">Copies the content of the specified file into the designated record field as stream data.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="0dfe8-124">Propiedades</span><span class="sxs-lookup"><span data-stu-id="0dfe8-124">Properties</span></span>

<span data-ttu-id="0dfe8-125">El objeto de **registro** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="0dfe8-125">The **Record** object has these properties.</span></span>



| <span data-ttu-id="0dfe8-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="0dfe8-126">Property</span></span>                                             | <span data-ttu-id="0dfe8-127">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="0dfe8-127">Access type</span></span>           | <span data-ttu-id="0dfe8-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="0dfe8-128">Description</span></span>                                                                                   |
|:-----------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0dfe8-129">**DataSize**</span><span class="sxs-lookup"><span data-stu-id="0dfe8-129">**DataSize**</span></span>](record-datasize.md)<br/>       |                       | <span data-ttu-id="0dfe8-130">Devuelve el tamaño de los datos del campo designado.</span><span class="sxs-lookup"><span data-stu-id="0dfe8-130">Returns the size of the data for the designated field.</span></span><br/>                             |
| [<span data-ttu-id="0dfe8-131">**FieldCount**</span><span class="sxs-lookup"><span data-stu-id="0dfe8-131">**FieldCount**</span></span>](record-fieldcount.md)<br/>   |                       | <span data-ttu-id="0dfe8-132">Devuelve el número de campos del registro.</span><span class="sxs-lookup"><span data-stu-id="0dfe8-132">Returns the number of fields in the record.</span></span><br/>                                        |
| [<span data-ttu-id="0dfe8-133">**IntegerData**</span><span class="sxs-lookup"><span data-stu-id="0dfe8-133">**IntegerData**</span></span>](record-integerdata.md)<br/> | <span data-ttu-id="0dfe8-134">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="0dfe8-134">Read/write</span></span><br/> | <span data-ttu-id="0dfe8-135">Transfiere datos enteros de 32 bits dentro o fuera de un campo especificado en el registro.</span><span class="sxs-lookup"><span data-stu-id="0dfe8-135">Transfers 32-bit integer data in to or out of a specified field within the record.</span></span><br/> |
| [<span data-ttu-id="0dfe8-136">**IsNull**</span><span class="sxs-lookup"><span data-stu-id="0dfe8-136">**IsNull**</span></span>](record-isnull.md)<br/>           |                       | <span data-ttu-id="0dfe8-137">Devuelve true si el campo indicado es NULL y false si el campo contiene datos.</span><span class="sxs-lookup"><span data-stu-id="0dfe8-137">Returns True if the indicated field is null and False if the field contains data.</span></span><br/>  |
| [<span data-ttu-id="0dfe8-138">**StringData**</span><span class="sxs-lookup"><span data-stu-id="0dfe8-138">**StringData**</span></span>](record-stringdata.md)<br/>   | <span data-ttu-id="0dfe8-139">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="0dfe8-139">Read/write</span></span><br/> | <span data-ttu-id="0dfe8-140">Transfiere datos de cadena de entrada o salida de un campo especificado dentro del registro.</span><span class="sxs-lookup"><span data-stu-id="0dfe8-140">Transfers string data in to or out of a specified field within the record.</span></span><br/>         |



 

## <a name="requirements"></a><span data-ttu-id="0dfe8-141">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0dfe8-141">Requirements</span></span>



| <span data-ttu-id="0dfe8-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="0dfe8-142">Requirement</span></span> | <span data-ttu-id="0dfe8-143">Value</span><span class="sxs-lookup"><span data-stu-id="0dfe8-143">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0dfe8-144">Versión</span><span class="sxs-lookup"><span data-stu-id="0dfe8-144">Version</span></span><br/> | <span data-ttu-id="0dfe8-145">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="0dfe8-145">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="0dfe8-146">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="0dfe8-146">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="0dfe8-147">Windows Installer en Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="0dfe8-147">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="0dfe8-148">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="0dfe8-148">DLL</span></span><br/>     | <dl> <span data-ttu-id="0dfe8-149"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0dfe8-149"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="0dfe8-150">IID</span><span class="sxs-lookup"><span data-stu-id="0dfe8-150">IID</span></span><br/>     | <span data-ttu-id="0dfe8-151">IID \_ IRecord se define como 000C1093-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="0dfe8-151">IID\_IRecord is defined as 000C1093-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                              |



## <a name="see-also"></a><span data-ttu-id="0dfe8-152">Vea también</span><span class="sxs-lookup"><span data-stu-id="0dfe8-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0dfe8-153">**Método CreateRecord**</span><span class="sxs-lookup"><span data-stu-id="0dfe8-153">**CreateRecord Method**</span></span>](installer-createrecord.md)
</dt> <dt>

[<span data-ttu-id="0dfe8-154">Ejemplos de scripting Windows Installer</span><span class="sxs-lookup"><span data-stu-id="0dfe8-154">Windows Installer Scripting Examples</span></span>](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




