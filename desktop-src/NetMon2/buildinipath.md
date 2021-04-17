---
description: La función BuildINIPath devuelve una ruta de acceso completa a un archivo INI que corresponde a la información que especifique.
ms.assetid: 214ce89c-8bb2-4e1a-872a-026743a3e3a6
title: Función BuildINIPath (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BuildINIPath
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 3f715e740319515fe4772d1a9905a2f9b563f3cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667743"
---
# <a name="buildinipath-function"></a>BuildINIPath función)

La función **BuildINIPath** devuelve una ruta de acceso completa a un archivo ini que corresponde a la información que especifique.

## <a name="syntax"></a>Sintaxis


```C++
LPSTR BuildINIPath(
   char *FullPath,
   char *IniFileName
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*FullPath* 
</dt> <dd>

Búfer que recibe el nombre de archivo INI completo.

</dd> <dt>

*IniFileName* 
</dt> <dd>

Nombre del archivo INI (el nombre de archivo completo menos la extensión de nombre de archivo).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es un puntero al nombre de archivo INI completo.

Si la función no se realiza correctamente, el valor devuelto es **null**.

## <a name="remarks"></a>Observaciones

La ruta de acceso que devuelve esta función es una ruta de acceso completa a un archivo INI que corresponde a la información especificada. Por ejemplo, si especifica XNS o TCP, la función genera una ruta de acceso a Xns.ini o Tcp.ini, respectivamente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                            |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Netmon. h</dt> </dl>   |
| Biblioteca<br/>                  | <dl> <dt>Analizador. lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl>  |



 

 




