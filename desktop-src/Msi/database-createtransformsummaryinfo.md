---
description: El método CreateTransformSummaryInfo del objeto de base de datos crea y rellena la secuencia de información de Resumen de un archivo de transformación existente. Este método rellena las propiedades con la base y el ProductCode y el ProductVersion de referencia.
ms.assetid: 67df9b9c-0e7c-49a6-a35e-5196327d6aff
title: Database. CreateTransformSummaryInfo (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.CreateTransformSummaryInfo
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 824f46fd17eb51fddbf09c2f34569574c50c570a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670687"
---
# <a name="databasecreatetransformsummaryinfo-method"></a><span data-ttu-id="d97b1-104">Database. CreateTransformSummaryInfo (método)</span><span class="sxs-lookup"><span data-stu-id="d97b1-104">Database.CreateTransformSummaryInfo method</span></span>

<span data-ttu-id="d97b1-105">El método **CreateTransformSummaryInfo** del objeto de [**base de datos**](database-object.md) crea y rellena la secuencia de información de Resumen de un archivo de transformación existente.</span><span class="sxs-lookup"><span data-stu-id="d97b1-105">The **CreateTransformSummaryInfo** method of the [**Database**](database-object.md) object creates and populates the summary information stream of an existing transform file.</span></span> <span data-ttu-id="d97b1-106">Este método rellena las propiedades con la base y el [**ProductCode**](productcode.md) y el [**ProductVersion**](productversion.md)de referencia.</span><span class="sxs-lookup"><span data-stu-id="d97b1-106">This method fills in the properties with the base and reference [**ProductCode**](productcode.md) and [**ProductVersion**](productversion.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="d97b1-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d97b1-107">Syntax</span></span>


```JScript
Database.CreateTransformSummaryInfo(
  reference,
  storage,
  errorConditions,
  validation
)
```



## <a name="parameters"></a><span data-ttu-id="d97b1-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d97b1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d97b1-109">*reference*</span><span class="sxs-lookup"><span data-stu-id="d97b1-109">*reference*</span></span> 
</dt> <dd>

<span data-ttu-id="d97b1-110">Base de datos necesaria que no incluye los cambios.</span><span class="sxs-lookup"><span data-stu-id="d97b1-110">Required database that does not include the changes.</span></span>

</dd> <dt>

<span data-ttu-id="d97b1-111">*storage*</span><span class="sxs-lookup"><span data-stu-id="d97b1-111">*storage*</span></span> 
</dt> <dd>

<span data-ttu-id="d97b1-112">Nombre del archivo de transformación generado.</span><span class="sxs-lookup"><span data-stu-id="d97b1-112">The name of the generated transform file.</span></span> <span data-ttu-id="d97b1-113">Esto es opcional.</span><span class="sxs-lookup"><span data-stu-id="d97b1-113">This is optional.</span></span>

</dd> <dt>

<span data-ttu-id="d97b1-114">*errorConditions*</span><span class="sxs-lookup"><span data-stu-id="d97b1-114">*errorConditions*</span></span> 
</dt> <dd>

<span data-ttu-id="d97b1-115">Condiciones de error necesarias que se deben suprimir cuando se aplica la transformación.</span><span class="sxs-lookup"><span data-stu-id="d97b1-115">Required error conditions that should be suppressed when the transform is applied.</span></span> <span data-ttu-id="d97b1-116">Combine uno o varios de los siguientes valores de condición de error.</span><span class="sxs-lookup"><span data-stu-id="d97b1-116">Combine one or more of the following error condition values.</span></span>



| <span data-ttu-id="d97b1-117">Nombre de condición de error</span><span class="sxs-lookup"><span data-stu-id="d97b1-117">Error condition name</span></span>                                                                                                                                                                                                                                                                                                                                        | <span data-ttu-id="d97b1-118">Significado</span><span class="sxs-lookup"><span data-stu-id="d97b1-118">Meaning</span></span>                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <span id="msiTransformErrorNone"></span><span id="msitransformerrornone"></span><span id="MSITRANSFORMERRORNONE"></span><dl> <span data-ttu-id="d97b1-119"><dt>**msiTransformErrorNone**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="d97b1-119"><dt>**msiTransformErrorNone**</dt> <dt>0</dt></span></span> </dl>                                                                         | <span data-ttu-id="d97b1-120">Ninguna de las siguientes condiciones.</span><span class="sxs-lookup"><span data-stu-id="d97b1-120">None of the following conditions.</span></span><br/>                                                |
| <span id="msiTransformErrorAddExistingRow"></span><span id="msitransformerroraddexistingrow"></span><span id="MSITRANSFORMERRORADDEXISTINGROW"></span><dl> <span data-ttu-id="d97b1-121"><dt>**msiTransformErrorAddExistingRow**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="d97b1-121"><dt>**msiTransformErrorAddExistingRow**</dt> <dt>1</dt></span></span> </dl>                                 | <span data-ttu-id="d97b1-122">Agrega una fila que ya existe.</span><span class="sxs-lookup"><span data-stu-id="d97b1-122">Adds a row that already exists.</span></span><br/>                                                  |
| <span id="msiTransformErrorDeleteNonExistingRow"></span><span id="msitransformerrordeletenonexistingrow"></span><span id="MSITRANSFORMERRORDELETENONEXISTINGROW"></span><dl> <span data-ttu-id="d97b1-123"><dt>**msiTransformErrorDeleteNonExistingRow**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="d97b1-123"><dt>**msiTransformErrorDeleteNonExistingRow**</dt> <dt>2</dt></span></span> </dl>         | <span data-ttu-id="d97b1-124">Elimina una fila que no existe.</span><span class="sxs-lookup"><span data-stu-id="d97b1-124">Deletes a row that does not exist.</span></span><br/>                                               |
| <span id="msiTransformErrorAddExistingTable"></span><span id="msitransformerroraddexistingtable"></span><span id="MSITRANSFORMERRORADDEXISTINGTABLE"></span><dl> <span data-ttu-id="d97b1-125"><dt>**msiTransformErrorAddExistingTable**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="d97b1-125"><dt>**msiTransformErrorAddExistingTable**</dt> <dt>4</dt></span></span> </dl>                         | <span data-ttu-id="d97b1-126">Agrega una tabla que ya existe.</span><span class="sxs-lookup"><span data-stu-id="d97b1-126">Adds a table that already exists.</span></span><br/>                                                |
| <span id="msiTransformErrorDeleteNonExistingTable"></span><span id="msitransformerrordeletenonexistingtable"></span><span id="MSITRANSFORMERRORDELETENONEXISTINGTABLE"></span><dl> <span data-ttu-id="d97b1-127"><dt>**msiTransformErrorDeleteNonExistingTable**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="d97b1-127"><dt>**msiTransformErrorDeleteNonExistingTable**</dt> <dt>8</dt></span></span> </dl> | <span data-ttu-id="d97b1-128">Elimina una tabla que no existe.</span><span class="sxs-lookup"><span data-stu-id="d97b1-128">Deletes a table that does not exist.</span></span><br/>                                             |
| <span id="msiTransformErrorUpdateNonExistingRow"></span><span id="msitransformerrorupdatenonexistingrow"></span><span id="MSITRANSFORMERRORUPDATENONEXISTINGROW"></span><dl> <span data-ttu-id="d97b1-129"><dt>**msiTransformErrorUpdateNonExistingRow**</dt> <dt>16</dt></span><span class="sxs-lookup"><span data-stu-id="d97b1-129"><dt>**msiTransformErrorUpdateNonExistingRow**</dt> <dt>16</dt></span></span> </dl>        | <span data-ttu-id="d97b1-130">Actualiza una fila que no existe.</span><span class="sxs-lookup"><span data-stu-id="d97b1-130">Updates a row that does not exist.</span></span><br/>                                               |
| <span id="msiTransformErrorChangeCodepage"></span><span id="msitransformerrorchangecodepage"></span><span id="MSITRANSFORMERRORCHANGECODEPAGE"></span><dl> <span data-ttu-id="d97b1-131"><dt>**msiTransformErrorChangeCodepage**</dt> <dt>32</dt></span><span class="sxs-lookup"><span data-stu-id="d97b1-131"><dt>**msiTransformErrorChangeCodepage**</dt> <dt>32</dt></span></span> </dl>                                | <span data-ttu-id="d97b1-132">Las páginas de códigos de base de datos y de transformación no coinciden y ninguna página de códigos es neutra.</span><span class="sxs-lookup"><span data-stu-id="d97b1-132">Transform and database code pages do not match and neither code page is neutral.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="d97b1-133">*validation*</span><span class="sxs-lookup"><span data-stu-id="d97b1-133">*validation*</span></span> 
</dt> <dd>

<span data-ttu-id="d97b1-134">Obligatorio cuando se aplica la transformación a una base de datos; muestra las propiedades que se deben validar para comprobar que esta transformación se puede aplicar a la base de datos.</span><span class="sxs-lookup"><span data-stu-id="d97b1-134">Required when the transform is applied to a database; shows which properties should be validated to verify that this transform can be applied to the database.</span></span> <span data-ttu-id="d97b1-135">Todas las propiedades se incluyen en el [conjunto de propiedades](summary-information-stream-property-set.md)de la secuencia de información de resumen.</span><span class="sxs-lookup"><span data-stu-id="d97b1-135">The properties are all contained in the [Summary Information Stream Property Set](summary-information-stream-property-set.md).</span></span>

<span data-ttu-id="d97b1-136">Combine uno o varios de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="d97b1-136">Combine one or more of the following values.</span></span>



| <span data-ttu-id="d97b1-137">Marca de validación</span><span class="sxs-lookup"><span data-stu-id="d97b1-137">Validation flag</span></span>                                                                                                                                                                                                                                                                                                         | <span data-ttu-id="d97b1-138">Significado</span><span class="sxs-lookup"><span data-stu-id="d97b1-138">Meaning</span></span>                                               |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <span id="msiTransformValidationNone"></span><span id="msitransformvalidationnone"></span><span id="MSITRANSFORMVALIDATIONNONE"></span><dl> <span data-ttu-id="d97b1-139"><dt>**msiTransformValidationNone**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="d97b1-139"><dt>**msiTransformValidationNone**</dt> <dt>0</dt></span></span> </dl>                 | <span data-ttu-id="d97b1-140">No se realiza ninguna validación.</span><span class="sxs-lookup"><span data-stu-id="d97b1-140">No validation done.</span></span><br/>                        |
| <span id="msiTransformValidationLanguage"></span><span id="msitransformvalidationlanguage"></span><span id="MSITRANSFORMVALIDATIONLANGUAGE"></span><dl> <span data-ttu-id="d97b1-141"><dt>**msiTransformValidationLanguage**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="d97b1-141"><dt>**msiTransformValidationLanguage**</dt> <dt>1</dt></span></span> </dl> | <span data-ttu-id="d97b1-142">El idioma predeterminado debe coincidir con la base de datos base.</span><span class="sxs-lookup"><span data-stu-id="d97b1-142">Default language must match base database.</span></span><br/> |
| <span id="msiTransformValidationProduct"></span><span id="msitransformvalidationproduct"></span><span id="MSITRANSFORMVALIDATIONPRODUCT"></span><dl> <span data-ttu-id="d97b1-143"><dt>**msiTransformValidationProduct**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="d97b1-143"><dt>**msiTransformValidationProduct**</dt> <dt>2</dt></span></span> </dl>     | <span data-ttu-id="d97b1-144">El producto debe coincidir con la base de datos base.</span><span class="sxs-lookup"><span data-stu-id="d97b1-144">Product must match base database.</span></span><br/>          |



 

<span data-ttu-id="d97b1-145">Para validar la versión del producto, primero elija una o varias de estas tres marcas para indicar qué parte de la versión se va a comprobar.</span><span class="sxs-lookup"><span data-stu-id="d97b1-145">To validate product version, first choose one or more of these three flags to indicate how much of the version is to be verified.</span></span>



| <span data-ttu-id="d97b1-146">Marca de validación</span><span class="sxs-lookup"><span data-stu-id="d97b1-146">Validation flag</span></span>                                                                                                                                                                                                                                                                                                              | <span data-ttu-id="d97b1-147">Significado</span><span class="sxs-lookup"><span data-stu-id="d97b1-147">Meaning</span></span>                                              |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <span id="msiTransformValidationMajorVer"></span><span id="msitransformvalidationmajorver"></span><span id="MSITRANSFORMVALIDATIONMAJORVER"></span><dl> <span data-ttu-id="d97b1-148"><dt>**msiTransformValidationMajorVer**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="d97b1-148"><dt>**msiTransformValidationMajorVer**</dt> <dt>8</dt></span></span> </dl>      | <span data-ttu-id="d97b1-149">Comprueba solo la versión principal.</span><span class="sxs-lookup"><span data-stu-id="d97b1-149">Checks major version only.</span></span><br/>                |
| <span id="msiTransformValidationMinorVer"></span><span id="msitransformvalidationminorver"></span><span id="MSITRANSFORMVALIDATIONMINORVER"></span><dl> <span data-ttu-id="d97b1-150"><dt>**msiTransformValidationMinorVer**</dt> <dt>16</dt></span><span class="sxs-lookup"><span data-stu-id="d97b1-150"><dt>**msiTransformValidationMinorVer**</dt> <dt>16</dt></span></span> </dl>     | <span data-ttu-id="d97b1-151">Comprueba solo la versión principal y secundaria.</span><span class="sxs-lookup"><span data-stu-id="d97b1-151">Checks major and minor version only.</span></span><br/>      |
| <span id="msiTransformValidationUpdateVer"></span><span id="msitransformvalidationupdatever"></span><span id="MSITRANSFORMVALIDATIONUPDATEVER"></span><dl> <span data-ttu-id="d97b1-152"><dt>**msiTransformValidationUpdateVer**</dt> <dt>32</dt></span><span class="sxs-lookup"><span data-stu-id="d97b1-152"><dt>**msiTransformValidationUpdateVer**</dt> <dt>32</dt></span></span> </dl> | <span data-ttu-id="d97b1-153">Comprueba las versiones principal, secundaria y de actualización.</span><span class="sxs-lookup"><span data-stu-id="d97b1-153">Checks major, minor, and update versions.</span></span><br/> |



 

<span data-ttu-id="d97b1-154">A continuación, elija una de las siguientes opciones para indicar la relación necesaria entre la versión del producto de la base de datos a la que se aplica la transformación y la de la base de datos base.</span><span class="sxs-lookup"><span data-stu-id="d97b1-154">Then choose one of the following to indicate the required relationship between the product version of the database the transform is being applied to and that of the base database.</span></span>



| <span data-ttu-id="d97b1-155">Marca de validación</span><span class="sxs-lookup"><span data-stu-id="d97b1-155">Validation flag</span></span>                                                                                                                                                                                                                                                                                                                                   | <span data-ttu-id="d97b1-156">Significado</span><span class="sxs-lookup"><span data-stu-id="d97b1-156">Meaning</span></span>                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <span id="msiTransformValidationLess"></span><span id="msitransformvalidationless"></span><span id="MSITRANSFORMVALIDATIONLESS"></span><dl> <span data-ttu-id="d97b1-157"><dt>**msiTransformValidationLess**</dt> <dt>64</dt></span><span class="sxs-lookup"><span data-stu-id="d97b1-157"><dt>**msiTransformValidationLess**</dt> <dt>64</dt></span></span> </dl>                                          | <span data-ttu-id="d97b1-158">Versión aplicada < versión base</span><span class="sxs-lookup"><span data-stu-id="d97b1-158">Applied version < base version</span></span><br/>  |
| <span id="msiTransformValidationLessOrEqual"></span><span id="msitransformvalidationlessorequal"></span><span id="MSITRANSFORMVALIDATIONLESSOREQUAL"></span><dl> <span data-ttu-id="d97b1-159"><dt>**msiTransformValidationLessOrEqual**</dt> <dt>128</dt></span><span class="sxs-lookup"><span data-stu-id="d97b1-159"><dt>**msiTransformValidationLessOrEqual**</dt> <dt>128</dt></span></span> </dl>             | <span data-ttu-id="d97b1-160">Versión aplicada <= versión base</span><span class="sxs-lookup"><span data-stu-id="d97b1-160">Applied version <= base version</span></span><br/> |
| <span id="msiTransformValidationEqual"></span><span id="msitransformvalidationequal"></span><span id="MSITRANSFORMVALIDATIONEQUAL"></span><dl> <span data-ttu-id="d97b1-161"><dt>**msiTransformValidationEqual**</dt> <dt>256</dt></span><span class="sxs-lookup"><span data-stu-id="d97b1-161"><dt>**msiTransformValidationEqual**</dt> <dt>256</dt></span></span> </dl>                                     | <span data-ttu-id="d97b1-162">Versión aplicada = versión base</span><span class="sxs-lookup"><span data-stu-id="d97b1-162">Applied version = base version</span></span><br/>     |
| <span id="msiTransformValidationGreaterOrEqual"></span><span id="msitransformvalidationgreaterorequal"></span><span id="MSITRANSFORMVALIDATIONGREATEROREQUAL"></span><dl> <span data-ttu-id="d97b1-163"><dt>**msiTransformValidationGreaterOrEqual**</dt> <dt>512</dt></span><span class="sxs-lookup"><span data-stu-id="d97b1-163"><dt>**msiTransformValidationGreaterOrEqual**</dt> <dt>512</dt></span></span> </dl> | <span data-ttu-id="d97b1-164">Versión aplicada >= versión base</span><span class="sxs-lookup"><span data-stu-id="d97b1-164">Applied version >= base version</span></span><br/> |
| <span id="msiTransformValidationGreater"></span><span id="msitransformvalidationgreater"></span><span id="MSITRANSFORMVALIDATIONGREATER"></span><dl> <span data-ttu-id="d97b1-165"><dt>**msiTransformValidationGreater**</dt> <dt>1024</dt></span><span class="sxs-lookup"><span data-stu-id="d97b1-165"><dt>**msiTransformValidationGreater**</dt> <dt>1024</dt></span></span> </dl>                            | <span data-ttu-id="d97b1-166">Versión aplicada > versión base</span><span class="sxs-lookup"><span data-stu-id="d97b1-166">Applied version > base version</span></span><br/>  |



 

<span data-ttu-id="d97b1-167">Para validar que la transformación se aplica a un paquete que tiene el [**UpgradeCode**](upgradecode.md)adecuado, establezca la marca siguiente.</span><span class="sxs-lookup"><span data-stu-id="d97b1-167">To validate that the transform is being applied to a package having the appropriate [**UpgradeCode**](upgradecode.md), set the following flag.</span></span>



| <span data-ttu-id="d97b1-168">Marca de validación</span><span class="sxs-lookup"><span data-stu-id="d97b1-168">Validation flag</span></span>                                                                                                                                                                                                                                                                                                                        | <span data-ttu-id="d97b1-169">Significado</span><span class="sxs-lookup"><span data-stu-id="d97b1-169">Meaning</span></span>                                                                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <span id="msiTransformValidationUpgradeCode"></span><span id="msitransformvalidationupgradecode"></span><span id="MSITRANSFORMVALIDATIONUPGRADECODE"></span><dl> <span data-ttu-id="d97b1-170"><dt>**msiTransformValidationUpgradeCode**</dt> <dt>2048</dt></span><span class="sxs-lookup"><span data-stu-id="d97b1-170"><dt>**msiTransformValidationUpgradeCode**</dt> <dt>2048</dt></span></span> </dl> | <span data-ttu-id="d97b1-171">Valida que la transformación es el [**UpgradeCode**](upgradecode.md)adecuado.</span><span class="sxs-lookup"><span data-stu-id="d97b1-171">Validates that the transform is the appropriate [**UpgradeCode**](upgradecode.md).</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d97b1-172">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d97b1-172">Return value</span></span>

<span data-ttu-id="d97b1-173">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="d97b1-173">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d97b1-174">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d97b1-174">Remarks</span></span>

<span data-ttu-id="d97b1-175">Para crear una secuencia de información de resumen para una transformación, las propiedades [**ProductCode**](productcode.md) y [**ProductVersion**](productversion.md) deben definirse en las tablas de [propiedades](property-table.md) de las bases de datos base y de referencia.</span><span class="sxs-lookup"><span data-stu-id="d97b1-175">To create a summary information stream for a transform, the [**ProductCode**](productcode.md) and [**ProductVersion**](productversion.md) properties must be defined in the [Property](property-table.md) tables of both the base and reference databases.</span></span> <span data-ttu-id="d97b1-176">Si se usa msiTransformValidationUpgradeCode, la propiedad [**UpgradeCode**](upgradecode.md) debe definirse en ambas bases de datos.</span><span class="sxs-lookup"><span data-stu-id="d97b1-176">If msiTransformValidationUpgradeCode is used, the [**UpgradeCode**](upgradecode.md) property must be defined in both databases.</span></span>

## <a name="requirements"></a><span data-ttu-id="d97b1-177">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d97b1-177">Requirements</span></span>



| <span data-ttu-id="d97b1-178">Requisito</span><span class="sxs-lookup"><span data-stu-id="d97b1-178">Requirement</span></span> | <span data-ttu-id="d97b1-179">Value</span><span class="sxs-lookup"><span data-stu-id="d97b1-179">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d97b1-180">Versión</span><span class="sxs-lookup"><span data-stu-id="d97b1-180">Version</span></span><br/> | <span data-ttu-id="d97b1-181">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="d97b1-181">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="d97b1-182">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="d97b1-182">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="d97b1-183">Windows Installer en Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="d97b1-183">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="d97b1-184">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d97b1-184">DLL</span></span><br/>     | <dl> <span data-ttu-id="d97b1-185"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d97b1-185"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="d97b1-186">IID</span><span class="sxs-lookup"><span data-stu-id="d97b1-186">IID</span></span><br/>     | <span data-ttu-id="d97b1-187">IID \_ IDatabase se define como 000C109D-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="d97b1-187">IID\_IDatabase is defined as 000C109D-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                            |



## <a name="see-also"></a><span data-ttu-id="d97b1-188">Vea también</span><span class="sxs-lookup"><span data-stu-id="d97b1-188">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d97b1-189">Transformaciones de base de datos</span><span class="sxs-lookup"><span data-stu-id="d97b1-189">Database Transforms</span></span>](database-transforms.md)
</dt> </dl>

 

 




