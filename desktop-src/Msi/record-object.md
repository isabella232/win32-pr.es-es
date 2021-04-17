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
# <a name="record-object"></a>Objeto record

El objeto de **registro** es un contenedor para almacenar y transferir un número variable de valores. Los campos del registro se indizan numéricamente y pueden contener cadenas, enteros, objetos y valores NULL. Los campos más allá del tamaño del registro asignado se tratan como si tuvieran valores NULL de forma permanente. El número de campo 0 está reservado.

## <a name="members"></a>Miembros

El objeto de **registro** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

El objeto de **registro** tiene estos métodos.



| Método                                  | Descripción                                                                                          |
|:----------------------------------------|:-----------------------------------------------------------------------------------------------------|
| [**ClearData**](record-cleardata.md)   | Borra los datos de todos los campos y los establece en NULL.<br/>                                      |
| [**FormatText**](record-formattext.md) | Da formato a los campos según la plantilla del campo 0.<br/>                                      |
| [**ReadStream**](record-readstream.md) | Lee un número especificado de bytes de un campo de registro que contiene los datos de la secuencia.<br/>                |
| [**SetStream**](record-setstream.md)   | Copia el contenido del archivo especificado en el campo de registro designado como datos de flujo.<br/> |



 

### <a name="properties"></a>Propiedades

El objeto de **registro** tiene estas propiedades.



| Propiedad                                             | Tipo de acceso           | Descripción                                                                                   |
|:-----------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------|
| [**DataSize**](record-datasize.md)<br/>       |                       | Devuelve el tamaño de los datos del campo designado.<br/>                             |
| [**FieldCount**](record-fieldcount.md)<br/>   |                       | Devuelve el número de campos del registro.<br/>                                        |
| [**IntegerData**](record-integerdata.md)<br/> | Lectura/escritura<br/> | Transfiere datos enteros de 32 bits dentro o fuera de un campo especificado en el registro.<br/> |
| [**IsNull**](record-isnull.md)<br/>           |                       | Devuelve true si el campo indicado es NULL y false si el campo contiene datos.<br/>  |
| [**StringData**](record-stringdata.md)<br/>   | Lectura/escritura<br/> | Transfiere datos de cadena de entrada o salida de un campo especificado dentro del registro.<br/>         |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IRecord se define como 000C1093-0000-0000-C000-000000000046<br/>                                                                                                                                                                              |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Método CreateRecord**](installer-createrecord.md)
</dt> <dt>

[Ejemplos de scripting Windows Installer](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




