---
description: El método GetError del objeto View devuelve el error de validación y el nombre de columna para los que se produjo el error.
ms.assetid: ca90dfa5-8e15-490c-835b-c5c225c3cc7b
title: View. GetError (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- View.GetError
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 1305bf6f497e92ff4d455a696179a943df8a057b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653481"
---
# <a name="viewgeterror-method"></a>View. GetError (método)

El método **GetError** del objeto [**View**](view-object.md) devuelve el error de validación y el nombre de columna para los que se produjo el error. En Automation, el valor devuelto es una cadena con el formato \# \# columnName, donde \# \# representa un código de error de 2 dígitos. Devuelve el primer error en la matriz de errores de la vista. las llamadas subsiguientes devuelven el siguiente valor en la matriz de errores. Una vez que se devuelve el valor ' 00 ', no existen más errores y las llamadas subsiguientes simplemente recorren en bucle la matriz.

## <a name="syntax"></a>Sintaxis


```JScript
View.GetError()
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ iView se define como 000C109C-0000-0000-C000-000000000046<br/>                                                                                                                                                                                |



 

 




