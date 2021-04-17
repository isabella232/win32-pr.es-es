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
# <a name="databasecreatetransformsummaryinfo-method"></a>Database. CreateTransformSummaryInfo (método)

El método **CreateTransformSummaryInfo** del objeto de [**base de datos**](database-object.md) crea y rellena la secuencia de información de Resumen de un archivo de transformación existente. Este método rellena las propiedades con la base y el [**ProductCode**](productcode.md) y el [**ProductVersion**](productversion.md)de referencia.

## <a name="syntax"></a>Sintaxis


```JScript
Database.CreateTransformSummaryInfo(
  reference,
  storage,
  errorConditions,
  validation
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*reference* 
</dt> <dd>

Base de datos necesaria que no incluye los cambios.

</dd> <dt>

*storage* 
</dt> <dd>

Nombre del archivo de transformación generado. Esto es opcional.

</dd> <dt>

*errorConditions* 
</dt> <dd>

Condiciones de error necesarias que se deben suprimir cuando se aplica la transformación. Combine uno o varios de los siguientes valores de condición de error.



| Nombre de condición de error                                                                                                                                                                                                                                                                                                                                        | Significado                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <span id="msiTransformErrorNone"></span><span id="msitransformerrornone"></span><span id="MSITRANSFORMERRORNONE"></span><dl> <dt>**msiTransformErrorNone**</dt> <dt>0</dt> </dl>                                                                         | Ninguna de las siguientes condiciones.<br/>                                                |
| <span id="msiTransformErrorAddExistingRow"></span><span id="msitransformerroraddexistingrow"></span><span id="MSITRANSFORMERRORADDEXISTINGROW"></span><dl> <dt>**msiTransformErrorAddExistingRow**</dt> <dt>1</dt> </dl>                                 | Agrega una fila que ya existe.<br/>                                                  |
| <span id="msiTransformErrorDeleteNonExistingRow"></span><span id="msitransformerrordeletenonexistingrow"></span><span id="MSITRANSFORMERRORDELETENONEXISTINGROW"></span><dl> <dt>**msiTransformErrorDeleteNonExistingRow**</dt> <dt>2</dt> </dl>         | Elimina una fila que no existe.<br/>                                               |
| <span id="msiTransformErrorAddExistingTable"></span><span id="msitransformerroraddexistingtable"></span><span id="MSITRANSFORMERRORADDEXISTINGTABLE"></span><dl> <dt>**msiTransformErrorAddExistingTable**</dt> <dt>4</dt> </dl>                         | Agrega una tabla que ya existe.<br/>                                                |
| <span id="msiTransformErrorDeleteNonExistingTable"></span><span id="msitransformerrordeletenonexistingtable"></span><span id="MSITRANSFORMERRORDELETENONEXISTINGTABLE"></span><dl> <dt>**msiTransformErrorDeleteNonExistingTable**</dt> <dt>8</dt> </dl> | Elimina una tabla que no existe.<br/>                                             |
| <span id="msiTransformErrorUpdateNonExistingRow"></span><span id="msitransformerrorupdatenonexistingrow"></span><span id="MSITRANSFORMERRORUPDATENONEXISTINGROW"></span><dl> <dt>**msiTransformErrorUpdateNonExistingRow**</dt> <dt>16</dt> </dl>        | Actualiza una fila que no existe.<br/>                                               |
| <span id="msiTransformErrorChangeCodepage"></span><span id="msitransformerrorchangecodepage"></span><span id="MSITRANSFORMERRORCHANGECODEPAGE"></span><dl> <dt>**msiTransformErrorChangeCodepage**</dt> <dt>32</dt> </dl>                                | Las páginas de códigos de base de datos y de transformación no coinciden y ninguna página de códigos es neutra.<br/> |



 

</dd> <dt>

*validation* 
</dt> <dd>

Obligatorio cuando se aplica la transformación a una base de datos; muestra las propiedades que se deben validar para comprobar que esta transformación se puede aplicar a la base de datos. Todas las propiedades se incluyen en el [conjunto de propiedades](summary-information-stream-property-set.md)de la secuencia de información de resumen.

Combine uno o varios de los valores siguientes.



| Marca de validación                                                                                                                                                                                                                                                                                                         | Significado                                               |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <span id="msiTransformValidationNone"></span><span id="msitransformvalidationnone"></span><span id="MSITRANSFORMVALIDATIONNONE"></span><dl> <dt>**msiTransformValidationNone**</dt> <dt>0</dt> </dl>                 | No se realiza ninguna validación.<br/>                        |
| <span id="msiTransformValidationLanguage"></span><span id="msitransformvalidationlanguage"></span><span id="MSITRANSFORMVALIDATIONLANGUAGE"></span><dl> <dt>**msiTransformValidationLanguage**</dt> <dt>1</dt> </dl> | El idioma predeterminado debe coincidir con la base de datos base.<br/> |
| <span id="msiTransformValidationProduct"></span><span id="msitransformvalidationproduct"></span><span id="MSITRANSFORMVALIDATIONPRODUCT"></span><dl> <dt>**msiTransformValidationProduct**</dt> <dt>2</dt> </dl>     | El producto debe coincidir con la base de datos base.<br/>          |



 

Para validar la versión del producto, primero elija una o varias de estas tres marcas para indicar qué parte de la versión se va a comprobar.



| Marca de validación                                                                                                                                                                                                                                                                                                              | Significado                                              |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <span id="msiTransformValidationMajorVer"></span><span id="msitransformvalidationmajorver"></span><span id="MSITRANSFORMVALIDATIONMAJORVER"></span><dl> <dt>**msiTransformValidationMajorVer**</dt> <dt>8</dt> </dl>      | Comprueba solo la versión principal.<br/>                |
| <span id="msiTransformValidationMinorVer"></span><span id="msitransformvalidationminorver"></span><span id="MSITRANSFORMVALIDATIONMINORVER"></span><dl> <dt>**msiTransformValidationMinorVer**</dt> <dt>16</dt> </dl>     | Comprueba solo la versión principal y secundaria.<br/>      |
| <span id="msiTransformValidationUpdateVer"></span><span id="msitransformvalidationupdatever"></span><span id="MSITRANSFORMVALIDATIONUPDATEVER"></span><dl> <dt>**msiTransformValidationUpdateVer**</dt> <dt>32</dt> </dl> | Comprueba las versiones principal, secundaria y de actualización.<br/> |



 

A continuación, elija una de las siguientes opciones para indicar la relación necesaria entre la versión del producto de la base de datos a la que se aplica la transformación y la de la base de datos base.



| Marca de validación                                                                                                                                                                                                                                                                                                                                   | Significado                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <span id="msiTransformValidationLess"></span><span id="msitransformvalidationless"></span><span id="MSITRANSFORMVALIDATIONLESS"></span><dl> <dt>**msiTransformValidationLess**</dt> <dt>64</dt> </dl>                                          | Versión aplicada < versión base<br/>  |
| <span id="msiTransformValidationLessOrEqual"></span><span id="msitransformvalidationlessorequal"></span><span id="MSITRANSFORMVALIDATIONLESSOREQUAL"></span><dl> <dt>**msiTransformValidationLessOrEqual**</dt> <dt>128</dt> </dl>             | Versión aplicada <= versión base<br/> |
| <span id="msiTransformValidationEqual"></span><span id="msitransformvalidationequal"></span><span id="MSITRANSFORMVALIDATIONEQUAL"></span><dl> <dt>**msiTransformValidationEqual**</dt> <dt>256</dt> </dl>                                     | Versión aplicada = versión base<br/>     |
| <span id="msiTransformValidationGreaterOrEqual"></span><span id="msitransformvalidationgreaterorequal"></span><span id="MSITRANSFORMVALIDATIONGREATEROREQUAL"></span><dl> <dt>**msiTransformValidationGreaterOrEqual**</dt> <dt>512</dt> </dl> | Versión aplicada >= versión base<br/> |
| <span id="msiTransformValidationGreater"></span><span id="msitransformvalidationgreater"></span><span id="MSITRANSFORMVALIDATIONGREATER"></span><dl> <dt>**msiTransformValidationGreater**</dt> <dt>1024</dt> </dl>                            | Versión aplicada > versión base<br/>  |



 

Para validar que la transformación se aplica a un paquete que tiene el [**UpgradeCode**](upgradecode.md)adecuado, establezca la marca siguiente.



| Marca de validación                                                                                                                                                                                                                                                                                                                        | Significado                                                                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <span id="msiTransformValidationUpgradeCode"></span><span id="msitransformvalidationupgradecode"></span><span id="MSITRANSFORMVALIDATIONUPGRADECODE"></span><dl> <dt>**msiTransformValidationUpgradeCode**</dt> <dt>2048</dt> </dl> | Valida que la transformación es el [**UpgradeCode**](upgradecode.md)adecuado.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Para crear una secuencia de información de resumen para una transformación, las propiedades [**ProductCode**](productcode.md) y [**ProductVersion**](productversion.md) deben definirse en las tablas de [propiedades](property-table.md) de las bases de datos base y de referencia. Si se usa msiTransformValidationUpgradeCode, la propiedad [**UpgradeCode**](upgradecode.md) debe definirse en ambas bases de datos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IDatabase se define como 000C109D-0000-0000-C000-000000000046<br/>                                                                                                                                                                            |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Transformaciones de base de datos](database-transforms.md)
</dt> </dl>

 

 




