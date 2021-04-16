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
# <a name="databaseapplytransform-method"></a>Database. ApplyTransform (método)

El método **ApplyTransform** del objeto de [**base de datos**](database-object.md) aplica la transformación a esta base de datos.

## <a name="syntax"></a>Sintaxis


```JScript
Database.ApplyTransform(
  storage,
  errorConditions
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*storage* 
</dt> <dd>

Ruta de acceso al archivo de transformación que se va a aplicar. Este parámetro es necesario.

</dd> <dt>

*errorConditions* 
</dt> <dd>

Especifica las condiciones de error que se van a suprimir. Especifique como una combinación de los siguientes valores enteros.



| Condición de error                                                                                                                                                                                                                                                                                                                                                  | Significado                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <span id="msiTransformErrorAddExistingRow"></span><span id="msitransformerroraddexistingrow"></span><span id="MSITRANSFORMERRORADDEXISTINGROW"></span><dl> <dt>**msiTransformErrorAddExistingRow**</dt> <dt>0x0001</dt> </dl>                                 | Agrega una fila que ya existe.<br/>                                                     |
| <span id="msiTransformErrorDeleteNonExistingRow"></span><span id="msitransformerrordeletenonexistingrow"></span><span id="MSITRANSFORMERRORDELETENONEXISTINGROW"></span><dl> <dt>**msiTransformErrorDeleteNonExistingRow**</dt> <dt>0x0002</dt> </dl>         | Elimina una fila que no existe.<br/>                                                  |
| <span id="msiTransformErrorAddExistingTable"></span><span id="msitransformerroraddexistingtable"></span><span id="MSITRANSFORMERRORADDEXISTINGTABLE"></span><dl> <dt>**msiTransformErrorAddExistingTable**</dt> <dt>0x0004</dt> </dl>                         | Agrega una tabla que ya existe.<br/>                                                   |
| <span id="msiTransformErrorDeleteNonExistingTable"></span><span id="msitransformerrordeletenonexistingtable"></span><span id="MSITRANSFORMERRORDELETENONEXISTINGTABLE"></span><dl> <dt>**msiTransformErrorDeleteNonExistingTable**</dt> <dt>0x0008</dt> </dl> | Elimina una tabla que no existe.<br/>                                                |
| <span id="msiTransformErrorUpdateNonExistingRow"></span><span id="msitransformerrorupdatenonexistingrow"></span><span id="MSITRANSFORMERRORUPDATENONEXISTINGROW"></span><dl> <dt>**msiTransformErrorUpdateNonExistingRow**</dt> <dt>0x0010</dt> </dl>         | Actualiza una fila que no existe.<br/>                                                  |
| <span id="msiTransformErrorChangeCodePage"></span><span id="msitransformerrorchangecodepage"></span><span id="MSITRANSFORMERRORCHANGECODEPAGE"></span><dl> <dt>**msiTransformErrorChangeCodePage**</dt> <dt>0x0020</dt> </dl>                                 | Las páginas de códigos de base de datos y de transformación no coinciden y ninguna tiene una página de códigos neutra.<br/> |
| <span id="msiTransformErrorViewTransform"></span><span id="msitransformerrorviewtransform"></span><span id="MSITRANSFORMERRORVIEWTRANSFORM"></span><dl> <dt>**msiTransformErrorViewTransform**</dt> <dt>0x0100</dt> </dl>                                     | Crea la [ \_ tabla temporal TransformView](-transformview-table.md).<br/>            |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

El método **ApplyTransform** retrasa las transformaciones hasta el último momento posible. Los pasos que se han llevado a cabo en **ApplyTransform** son la transformación inmediata de los catálogos de tablas y columnas para la base de datos. Los catálogos de tablas y columnas se actualizan en función de la tabla que se agrega o se elimina y la columna que se agrega (no se permite la eliminación de columnas). Si una tabla está cargada actualmente en memoria y debe transformarse, se transforma. De lo contrario, el estado de la tabla se establece en que requiere una transformación de modo que, cuando se carga la tabla, o cuando la base de datos se confirma, se aplica la transformación. La transformación en esta instancia significa que se agregan, eliminan o actualizan los datos reales (filas) de la tabla.

Si se produce un error en el método, puede obtener información de error extendida mediante el método [**LastErrorRecord**](installer-lasterrorrecord.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IDatabase se define como 000C109D-0000-0000-C000-000000000046<br/>                                                                                                                                                                            |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Base de datos**](database-object.md)
</dt> <dt>

[Transformaciones de base de datos](database-transforms.md)
</dt> </dl>

 

 




