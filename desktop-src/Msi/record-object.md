---
description: El objeto Record es un contenedor para contener y transferir un número variable de valores.
ms.assetid: e832c19f-61a6-4e42-a10a-b7bb1705af59
title: Objeto Record
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
ms.openlocfilehash: 149abed4cc09b347c7d1ffabb27a139b448939188acd918aaadf2dccb345de1a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120041965"
---
# <a name="record-object"></a>Objeto Record

El **objeto Record** es un contenedor para contener y transferir un número variable de valores. Los campos del registro se indexa numéricamente y pueden contener cadenas, enteros, objetos y valores NULL. Los campos más allá del tamaño de registro asignado se tratan como que tienen valores NULL permanentes. El campo número 0 está reservado.

## <a name="members"></a>Miembros

El **objeto Record** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

El **objeto Record** tiene estos métodos.



| Método                                  | Descripción                                                                                          |
|:----------------------------------------|:-----------------------------------------------------------------------------------------------------|
| [**ClearData**](record-cleardata.md)   | Borra los datos de todos los campos y los establece en NULL.<br/>                                      |
| [**FormatText**](record-formattext.md) | Da formato a los campos según la plantilla del campo 0.<br/>                                      |
| [**ReadStream**](record-readstream.md) | Lee un número especificado de bytes de un campo de registro que contiene datos de flujo.<br/>                |
| [**SetStream**](record-setstream.md)   | Copia el contenido del archivo especificado en el campo de registro designado como datos de flujo.<br/> |



 

### <a name="properties"></a>Propiedades

El **objeto Record** tiene estas propiedades.



| Propiedad                                             | Tipo de acceso           | Descripción                                                                                   |
|:-----------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------|
| [**DataSize**](record-datasize.md)<br/>       |                       | Devuelve el tamaño de los datos del campo designado.<br/>                             |
| [**FieldCount**](record-fieldcount.md)<br/>   |                       | Devuelve el número de campos del registro.<br/>                                        |
| [**IntegerData**](record-integerdata.md)<br/> | Lectura/escritura<br/> | Transfiere datos enteros de 32 bits dentro o fuera de un campo especificado dentro del registro.<br/> |
| [**IsNull**](record-isnull.md)<br/>           |                       | Devuelve True si el campo indicado es NULL y False si el campo contiene datos.<br/>  |
| [**StringData**](record-stringdata.md)<br/>   | Lectura/escritura<br/> | Transfiere los datos de cadena dentro o fuera de un campo especificado dentro del registro.<br/>         |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4.0 o Windows Installer 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID IRecord se define como \_ 000C1093-0000-0000-C000-00000000046<br/>                                                                                                                                                                              |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CreateRecord (método)**](installer-createrecord.md)
</dt> <dt>

[Windows Ejemplos de scripting del instalador](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




