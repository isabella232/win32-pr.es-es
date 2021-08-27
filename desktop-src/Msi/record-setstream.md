---
description: El método SetStream del objeto Record copia el contenido del archivo especificado en el campo de registro designado como datos de flujo. Los datos de flujo no se pueden insertar en campos temporales.
ms.assetid: feb79371-d0c4-4bb0-b539-2f431ee1051b
title: Método Record.SetStream
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
ms.openlocfilehash: de443f2d6802fb74e4b0f05b90ca8d3b3f97e328991fde50ec05ff37c203943c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118626975"
---
# <a name="recordsetstream-method"></a>Método Record.SetStream

El **método SetStream** del [**objeto Record**](record-object.md) copia el contenido del archivo especificado en el campo de registro designado como datos de flujo. Los datos de flujo no se pueden insertar en campos temporales.

## <a name="syntax"></a>Sintaxis


```JScript
Record.SetStream(
  field,
  filePath
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Campo* 
</dt> <dd>

Número de campo requerido del valor dentro del registro, basado en 1.

</dd> <dt>

*Filepath* 
</dt> <dd>

Ubicación del archivo que se copiará. No se realiza ninguna traducción de ningún tipo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Si se produce un error en el método , puede obtener información de error extendida mediante el [**método LastErrorRecord.**](installer-lasterrorrecord.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4.0 o Windows Installer 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID IRecord se define como \_ 000C1093-0000-0000-C000-00000000046<br/>                                                                                                                                                                              |



 

 




