---
description: El objeto Record es un contenedor para contener y transferir un número variable de valores.
ms.assetid: e832c19f-61a6-4e42-a10a-b7bb1705af59
title: Objeto de registro
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069722"
---
# <a name="record-object"></a>Objeto de registro

El **objeto Record** es un contenedor para contener y transferir un número variable de valores. Los campos del registro están indizados numéricamente y pueden contener cadenas, enteros, objetos y valores NULL. Los campos más allá del tamaño de registro asignado se tratan como que tienen valores null permanentemente. El número de campo 0 está reservado.

## <a name="members"></a>Members

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
| [**IntegerData**](record-integerdata.md)<br/> | Lectura y escritura<br/> | Transfiere datos enteros de 32 bits dentro o fuera de un campo especificado dentro del registro.<br/> |
| [**IsNull**](record-isnull.md)<br/>           |                       | Devuelve True si el campo indicado es NULL y False si el campo contiene datos.<br/>  |
| [**StringData**](record-stringdata.md)<br/>   | Lectura y escritura<br/> | Transfiere los datos de cadena dentro o fuera de un campo especificado dentro del registro.<br/>         |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Instalador 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID IRecord se define como \_ 000C1093-0000-0000-C000-000000000046<br/>                                                                                                                                                                              |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CreateRecord (método)**](installer-createrecord.md)
</dt> <dt>

[Windows Ejemplos de scripting del instalador](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




