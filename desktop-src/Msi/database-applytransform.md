---
description: El método ApplyTransform del objeto Database aplica la transformación a esta base de datos.
ms.assetid: bcf1ea78-54ad-49d9-8fba-7b88ced236eb
title: Método Database.ApplyTransform
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127158657"
---
# <a name="databaseapplytransform-method"></a>Método Database.ApplyTransform

El **método ApplyTransform** del objeto [**Database**](database-object.md) aplica la transformación a esta base de datos.

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

Ruta de acceso al archivo de transformación que se está aplicando. Este parámetro es obligatorio.

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
| <span id="msiTransformErrorChangeCodePage"></span><span id="msitransformerrorchangecodepage"></span><span id="MSITRANSFORMERRORCHANGECODEPAGE"></span><dl> <dt>**msiTransformErrorChangeCodePage**</dt> <dt>0x0020</dt> </dl>                                 | Las páginas de códigos de transformación y base de datos no coinciden y ninguna tiene una página de códigos neutra.<br/> |
| <span id="msiTransformErrorViewTransform"></span><span id="msitransformerrorviewtransform"></span><span id="MSITRANSFORMERRORVIEWTRANSFORM"></span><dl> <dt>**msiTransformErrorViewTransform**</dt> <dt>0x0100</dt> </dl>                                     | Crea la tabla [ \_ transformView temporal](-transformview-table.md).<br/>            |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

El **método ApplyTransform** retrasa la transformación de tablas hasta el último momento posible. Los pasos que se han realizado **en ApplyTransform** son transformar inmediatamente los catálogos de tablas y columnas de la base de datos. Los catálogos de tablas y columnas se actualizan según la tabla que se agrega o elimina y la columna que se agrega (no se permite la eliminación de columnas). Si una tabla se carga actualmente en memoria y debe transformarse, se transforma. De lo contrario, el estado de la tabla se establece en que requiere una transformación para que, cuando se cargue la tabla o cuando se confirma la base de datos, se aplique la transformación. La transformación en esta instancia significa que los datos reales (fila) de la tabla se agregan, eliminan o actualizan.

Si se produce un error en el método , puede obtener información de error extendida mediante el [**método LastErrorRecord.**](installer-lasterrorrecord.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Instalador 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID IDatabase se define como \_ 000C109D-0000-0000-C000-000000000046<br/>                                                                                                                                                                            |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Base de datos**](database-object.md)
</dt> <dt>

[Transformaciones de base de datos](database-transforms.md)
</dt> </dl>

 

 




