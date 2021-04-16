---
description: El método ApplyTransform del objeto de base de datos aplica la transformación a esta base de datos.
ms.assetid: bcf1ea78-54ad-49d9-8fba-7b88ced236eb
title: Database. ApplyTransform (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.ApplyTransform
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 81eda2f2c868b4ccd637ec117850c2beea14eef9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671454"
---
# <a name="databaseapplytransform-method"></a><span data-ttu-id="7c8fa-103">Database. ApplyTransform (método)</span><span class="sxs-lookup"><span data-stu-id="7c8fa-103">Database.ApplyTransform method</span></span>

<span data-ttu-id="7c8fa-104">El método **ApplyTransform** del objeto de [**base de datos**](database-object.md) aplica la transformación a esta base de datos.</span><span class="sxs-lookup"><span data-stu-id="7c8fa-104">The **ApplyTransform** method of the [**Database**](database-object.md) object applies the transform to this database.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c8fa-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7c8fa-105">Syntax</span></span>


```JScript
Database.ApplyTransform(
  storage,
  errorConditions
)
```



## <a name="parameters"></a><span data-ttu-id="7c8fa-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7c8fa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7c8fa-107">*storage*</span><span class="sxs-lookup"><span data-stu-id="7c8fa-107">*storage*</span></span> 
</dt> <dd>

<span data-ttu-id="7c8fa-108">Ruta de acceso al archivo de transformación que se va a aplicar.</span><span class="sxs-lookup"><span data-stu-id="7c8fa-108">Path to the transform file being applied.</span></span> <span data-ttu-id="7c8fa-109">Este parámetro es necesario.</span><span class="sxs-lookup"><span data-stu-id="7c8fa-109">This parameter is required.</span></span>

</dd> <dt>

<span data-ttu-id="7c8fa-110">*errorConditions*</span><span class="sxs-lookup"><span data-stu-id="7c8fa-110">*errorConditions*</span></span> 
</dt> <dd>

<span data-ttu-id="7c8fa-111">Especifica las condiciones de error que se van a suprimir.</span><span class="sxs-lookup"><span data-stu-id="7c8fa-111">Specifies the error conditions that are to be suppressed.</span></span> <span data-ttu-id="7c8fa-112">Especifique como una combinación de los siguientes valores enteros.</span><span class="sxs-lookup"><span data-stu-id="7c8fa-112">Specify as a combination of the following integer values.</span></span>



| <span data-ttu-id="7c8fa-113">Condición de error</span><span class="sxs-lookup"><span data-stu-id="7c8fa-113">Error condition</span></span>                                                                                                                                                                                                                                                                                                                                                  | <span data-ttu-id="7c8fa-114">Significado</span><span class="sxs-lookup"><span data-stu-id="7c8fa-114">Meaning</span></span>                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <span id="msiTransformErrorAddExistingRow"></span><span id="msitransformerroraddexistingrow"></span><span id="MSITRANSFORMERRORADDEXISTINGROW"></span><dl> <span data-ttu-id="7c8fa-115"><dt>**msiTransformErrorAddExistingRow**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="7c8fa-115"><dt>**msiTransformErrorAddExistingRow**</dt> <dt>0x0001</dt></span></span> </dl>                                 | <span data-ttu-id="7c8fa-116">Agrega una fila que ya existe.</span><span class="sxs-lookup"><span data-stu-id="7c8fa-116">Adds a row that already exists.</span></span><br/>                                                     |
| <span id="msiTransformErrorDeleteNonExistingRow"></span><span id="msitransformerrordeletenonexistingrow"></span><span id="MSITRANSFORMERRORDELETENONEXISTINGROW"></span><dl> <span data-ttu-id="7c8fa-117"><dt>**msiTransformErrorDeleteNonExistingRow**</dt> <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="7c8fa-117"><dt>**msiTransformErrorDeleteNonExistingRow**</dt> <dt>0x0002</dt></span></span> </dl>         | <span data-ttu-id="7c8fa-118">Elimina una fila que no existe.</span><span class="sxs-lookup"><span data-stu-id="7c8fa-118">Deletes a row that does not exist.</span></span><br/>                                                  |
| <span id="msiTransformErrorAddExistingTable"></span><span id="msitransformerroraddexistingtable"></span><span id="MSITRANSFORMERRORADDEXISTINGTABLE"></span><dl> <span data-ttu-id="7c8fa-119"><dt>**msiTransformErrorAddExistingTable**</dt> <dt>0x0004</dt></span><span class="sxs-lookup"><span data-stu-id="7c8fa-119"><dt>**msiTransformErrorAddExistingTable**</dt> <dt>0x0004</dt></span></span> </dl>                         | <span data-ttu-id="7c8fa-120">Agrega una tabla que ya existe.</span><span class="sxs-lookup"><span data-stu-id="7c8fa-120">Adds a table that already exists.</span></span><br/>                                                   |
| <span id="msiTransformErrorDeleteNonExistingTable"></span><span id="msitransformerrordeletenonexistingtable"></span><span id="MSITRANSFORMERRORDELETENONEXISTINGTABLE"></span><dl> <span data-ttu-id="7c8fa-121"><dt>**msiTransformErrorDeleteNonExistingTable**</dt> <dt>0x0008</dt></span><span class="sxs-lookup"><span data-stu-id="7c8fa-121"><dt>**msiTransformErrorDeleteNonExistingTable**</dt> <dt>0x0008</dt></span></span> </dl> | <span data-ttu-id="7c8fa-122">Elimina una tabla que no existe.</span><span class="sxs-lookup"><span data-stu-id="7c8fa-122">Deletes a table that does not exist.</span></span><br/>                                                |
| <span id="msiTransformErrorUpdateNonExistingRow"></span><span id="msitransformerrorupdatenonexistingrow"></span><span id="MSITRANSFORMERRORUPDATENONEXISTINGROW"></span><dl> <span data-ttu-id="7c8fa-123"><dt>**msiTransformErrorUpdateNonExistingRow**</dt> <dt>0x0010</dt></span><span class="sxs-lookup"><span data-stu-id="7c8fa-123"><dt>**msiTransformErrorUpdateNonExistingRow**</dt> <dt>0x0010</dt></span></span> </dl>         | <span data-ttu-id="7c8fa-124">Actualiza una fila que no existe.</span><span class="sxs-lookup"><span data-stu-id="7c8fa-124">Updates a row that does not exist.</span></span><br/>                                                  |
| <span id="msiTransformErrorChangeCodePage"></span><span id="msitransformerrorchangecodepage"></span><span id="MSITRANSFORMERRORCHANGECODEPAGE"></span><dl> <span data-ttu-id="7c8fa-125"><dt>**msiTransformErrorChangeCodePage**</dt> <dt>0x0020</dt></span><span class="sxs-lookup"><span data-stu-id="7c8fa-125"><dt>**msiTransformErrorChangeCodePage**</dt> <dt>0x0020</dt></span></span> </dl>                                 | <span data-ttu-id="7c8fa-126">Las páginas de códigos de base de datos y de transformación no coinciden y ninguna tiene una página de códigos neutra.</span><span class="sxs-lookup"><span data-stu-id="7c8fa-126">Transform and database code pages do not match and neither has a neutral code page.</span></span><br/> |
| <span id="msiTransformErrorViewTransform"></span><span id="msitransformerrorviewtransform"></span><span id="MSITRANSFORMERRORVIEWTRANSFORM"></span><dl> <span data-ttu-id="7c8fa-127"><dt>**msiTransformErrorViewTransform**</dt> <dt>0x0100</dt></span><span class="sxs-lookup"><span data-stu-id="7c8fa-127"><dt>**msiTransformErrorViewTransform**</dt> <dt>0x0100</dt></span></span> </dl>                                     | <span data-ttu-id="7c8fa-128">Crea la [ \_ tabla temporal TransformView](-transformview-table.md).</span><span class="sxs-lookup"><span data-stu-id="7c8fa-128">Creates the temporary [\_TransformView table](-transformview-table.md).</span></span><br/>            |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7c8fa-129">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7c8fa-129">Return value</span></span>

<span data-ttu-id="7c8fa-130">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="7c8fa-130">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7c8fa-131">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7c8fa-131">Remarks</span></span>

<span data-ttu-id="7c8fa-132">El método **ApplyTransform** retrasa las transformaciones hasta el último momento posible.</span><span class="sxs-lookup"><span data-stu-id="7c8fa-132">The **ApplyTransform** method delays transforming tables until the last possible moment.</span></span> <span data-ttu-id="7c8fa-133">Los pasos que se han llevado a cabo en **ApplyTransform** son la transformación inmediata de los catálogos de tablas y columnas para la base de datos.</span><span class="sxs-lookup"><span data-stu-id="7c8fa-133">The steps taken in **ApplyTransform** are to immediately transform the table and column catalogs for the database.</span></span> <span data-ttu-id="7c8fa-134">Los catálogos de tablas y columnas se actualizan en función de la tabla que se agrega o se elimina y la columna que se agrega (no se permite la eliminación de columnas).</span><span class="sxs-lookup"><span data-stu-id="7c8fa-134">The table and column catalogs are updated according to which table is added or deleted and which column is added (no deletion of columns is allowed).</span></span> <span data-ttu-id="7c8fa-135">Si una tabla está cargada actualmente en memoria y debe transformarse, se transforma.</span><span class="sxs-lookup"><span data-stu-id="7c8fa-135">If a table is currently loaded in memory and needs to be transformed, it is transformed.</span></span> <span data-ttu-id="7c8fa-136">De lo contrario, el estado de la tabla se establece en que requiere una transformación de modo que, cuando se carga la tabla, o cuando la base de datos se confirma, se aplica la transformación.</span><span class="sxs-lookup"><span data-stu-id="7c8fa-136">Otherwise, the table state is set to that requiring a transform so that when the table is loaded, or when the database is committed, the transform is applied.</span></span> <span data-ttu-id="7c8fa-137">La transformación en esta instancia significa que se agregan, eliminan o actualizan los datos reales (filas) de la tabla.</span><span class="sxs-lookup"><span data-stu-id="7c8fa-137">Transform in this instance means that the actual (row) data of the table is added, deleted, or updated.</span></span>

<span data-ttu-id="7c8fa-138">Si se produce un error en el método, puede obtener información de error extendida mediante el método [**LastErrorRecord**](installer-lasterrorrecord.md) .</span><span class="sxs-lookup"><span data-stu-id="7c8fa-138">If the method fails, you can obtain extended error information by using the [**LastErrorRecord**](installer-lasterrorrecord.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="7c8fa-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7c8fa-139">Requirements</span></span>



| <span data-ttu-id="7c8fa-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="7c8fa-140">Requirement</span></span> | <span data-ttu-id="7c8fa-141">Value</span><span class="sxs-lookup"><span data-stu-id="7c8fa-141">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7c8fa-142">Versión</span><span class="sxs-lookup"><span data-stu-id="7c8fa-142">Version</span></span><br/> | <span data-ttu-id="7c8fa-143">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="7c8fa-143">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="7c8fa-144">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="7c8fa-144">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="7c8fa-145">Windows Installer en Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="7c8fa-145">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="7c8fa-146">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="7c8fa-146">DLL</span></span><br/>     | <dl> <span data-ttu-id="7c8fa-147"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7c8fa-147"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="7c8fa-148">IID</span><span class="sxs-lookup"><span data-stu-id="7c8fa-148">IID</span></span><br/>     | <span data-ttu-id="7c8fa-149">IID \_ IDatabase se define como 000C109D-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="7c8fa-149">IID\_IDatabase is defined as 000C109D-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                            |



## <a name="see-also"></a><span data-ttu-id="7c8fa-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="7c8fa-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c8fa-151">**Base de datos**</span><span class="sxs-lookup"><span data-stu-id="7c8fa-151">**Database**</span></span>](database-object.md)
</dt> <dt>

[<span data-ttu-id="7c8fa-152">Transformaciones de base de datos</span><span class="sxs-lookup"><span data-stu-id="7c8fa-152">Database Transforms</span></span>](database-transforms.md)
</dt> </dl>

 

 




