---
description: El método ReadStream del objeto record Lee un número especificado de bytes de un campo registro que contiene los datos de la secuencia.
ms.assetid: 845e23e5-6379-4592-aee4-cd6832baf335
title: Método record. ReadStream
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
ms.openlocfilehash: bc77e07231d086f15086662d60581d4c5992bf5b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670966"
---
# <a name="recordreadstream-method"></a>Método record. ReadStream

El método **ReadStream** del objeto [**Record**](record-object.md) Lee un número especificado de bytes de un campo registro que contiene los datos de la secuencia.

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

*campo* 
</dt> <dd>

El número de campo necesario del valor dentro del registro, basado en 1.

</dd> <dt>

*length* 
</dt> <dd>

Número necesario de bytes que se van a leer de la secuencia.

</dd> <dt>

*format* 
</dt> <dd>

Interpretación requerida y devolución de los bytes de datos.



| Nombre de parámetro                                                                                                                                                                                                                                                                  | Significado                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <span id="msiReadStreamInteger"></span><span id="msireadstreaminteger"></span><span id="MSIREADSTREAMINTEGER"></span><dl> <dt>**msiReadStreamInteger**</dt> <dt>0</dt> </dl> | Como entero largo, la longitud debe ser de 1 a 4.<br/>             |
| <span id="msiReadStreamBytes"></span><span id="msireadstreambytes"></span><span id="MSIREADSTREAMBYTES"></span><dl> <dt>**msiReadStreamBytes**</dt> <dt>1</dt> </dl>         | Los datos como un **BSTR**: un byte por carácter.<br/>           |
| <span id="msiReadStreamAnsi"></span><span id="msireadstreamansi"></span><span id="MSIREADSTREAMANSI"></span><dl> <dt>**msiReadStreamAnsi**</dt> <dt>2</dt> </dl>             | Bytes ANSI convertidos en un **BSTR** Unicode.<br/>         |
| <span id="msiReadStreamDirect"></span><span id="msireadstreamdirect"></span><span id="MSIREADSTREAMDIRECT"></span><dl> <dt>**msiReadStreamDirect**</dt> <dt>3</dt> </dl>     | Pares de bytes que se devuelven directamente como **BSTR**.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve una cadena que contiene el número solicitado de bytes leídos de un campo de registro.

## <a name="remarks"></a>Observaciones

El valor devuelto de un campo inexistente es un valor vacío. Si el flujo tiene menos bytes solicitados por el recuento, la cadena devuelta se acorta adecuadamente.

Para obtener un ejemplo de este método, vea [copiar un archivo ANSI en un campo de base de datos](copy-ansi-file-into-a-database-field.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IRecord se define como 000C1093-0000-0000-C000-000000000046<br/>                                                                                                                                                                              |



 

 




