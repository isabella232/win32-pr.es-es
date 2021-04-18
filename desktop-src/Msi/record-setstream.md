---
description: El método SetStream del objeto record copia el contenido del archivo especificado en el campo registro designado como datos de flujo. Los datos de flujo no se pueden insertar en campos temporales.
ms.assetid: feb79371-d0c4-4bb0-b539-2f431ee1051b
title: Método record. SetStream
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Record.SetStream
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 94ec3d63b3dcd75a13c2c0ff62b624b89979d641
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680760"
---
# <a name="recordsetstream-method"></a>Método record. SetStream

El método **SetStream** del objeto [**Record**](record-object.md) copia el contenido del archivo especificado en el campo registro designado como datos de flujo. Los datos de flujo no se pueden insertar en campos temporales.

## <a name="syntax"></a>Sintaxis


```JScript
Record.SetStream(
  field,
  filePath
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*campo* 
</dt> <dd>

Número de campo obligatorio del valor dentro del registro, basado en 1.

</dd> <dt>

*filePath* 
</dt> <dd>

Ubicación del archivo que se va a copiar. No se realiza ninguna conversión de ningún tipo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Si se produce un error en el método, puede obtener información de error extendida mediante el método [**LastErrorRecord**](installer-lasterrorrecord.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IRecord se define como 000C1093-0000-0000-C000-000000000046<br/>                                                                                                                                                                              |



 

 




