---
description: El método ReadStream del objeto Record lee un número especificado de bytes de un campo de registro que contiene datos de flujo.
ms.assetid: 845e23e5-6379-4592-aee4-cd6832baf335
title: Método Record.ReadStream
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Record.ReadStream
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 85f3cf97175b28750408d28a6e164f8aaa5fe71ec18bb89fff8e5c4583fb85cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120041945"
---
# <a name="recordreadstream-method"></a>Método Record.ReadStream

El **método ReadStream** del [**objeto Record**](record-object.md) lee un número especificado de bytes de un campo de registro que contiene datos de flujo.

## <a name="syntax"></a>Sintaxis


```JScript
Record.ReadStream(
  field,
  length,
  format
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Campo* 
</dt> <dd>

Número de campo necesario del valor dentro del registro, basado en 1.

</dd> <dt>

*length* 
</dt> <dd>

Número necesario de bytes que se leerán de la secuencia.

</dd> <dt>

*format* 
</dt> <dd>

Se requiere la interpretación y devolución de los bytes de datos.



| Nombre de parámetro                                                                                                                                                                                                                                                                  | Significado                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <span id="msiReadStreamInteger"></span><span id="msireadstreaminteger"></span><span id="MSIREADSTREAMINTEGER"></span><dl> <dt>**msiReadStreamInteger**</dt> <dt>0</dt> </dl> | Como entero largo, la longitud debe ser de 1 a 4.<br/>             |
| <span id="msiReadStreamBytes"></span><span id="msireadstreambytes"></span><span id="MSIREADSTREAMBYTES"></span><dl> <dt>**msiReadStreamBytes**</dt> <dt>1</dt> </dl>         | Los datos como **un BSTR**: un byte por carácter.<br/>           |
| <span id="msiReadStreamAnsi"></span><span id="msireadstreamansi"></span><span id="MSIREADSTREAMANSI"></span><dl> <dt>**msiReadStreamAnsi**</dt> <dt>2</dt> </dl>             | Bytes ANSI traducidos a un **BSTR unicode.**<br/>         |
| <span id="msiReadStreamDirect"></span><span id="msireadstreamdirect"></span><span id="MSIREADSTREAMDIRECT"></span><dl> <dt>**msiReadStreamDirect**</dt> <dt>3</dt> </dl>     | Pares de bytes que se devuelven directamente como **un BSTR**.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve una cadena que contiene el número solicitado de bytes leídos de un campo de registro.

## <a name="remarks"></a>Comentarios

El valor devuelto de un campo inexistente es un valor vacío. Si la secuencia tiene menos bytes que el recuento solicitado, la cadena devuelta se abrevia correctamente.

Para obtener un ejemplo de este método, vea [Copiar un archivo ANSI en un campo de base de datos](copy-ansi-file-into-a-database-field.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Instalador 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID IRecord se define como \_ 000C1093-0000-0000-C000-000000000046<br/>                                                                                                                                                                              |



 

 




