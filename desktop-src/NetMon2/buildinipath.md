---
description: La función BuildINIPath devuelve una ruta de acceso completa a un archivo INI que corresponde a la información que especifique.
ms.assetid: 214ce89c-8bb2-4e1a-872a-026743a3e3a6
title: Función BuildINIPath (Netmon.h)
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
ms.openlocfilehash: b75df338142ab0ec97db3e60cbba1b5f68df3e0e67947d4c13cdccccd409bdf8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119744704"
---
# <a name="buildinipath-function"></a>Función BuildINIPath

La **función BuildINIPath** devuelve una ruta de acceso completa a un archivo INI que corresponde a la información que especifique.

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

Nombre del archivo INI (nombre de archivo completo menos la extensión de nombre de archivo).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es un puntero al nombre de archivo INI completo.

Si la función no se realiza correctamente, el valor devuelto es **NULL.**

## <a name="remarks"></a>Comentarios

La ruta de acceso que devuelve esta función es una ruta de acceso completa a un archivo INI que corresponde a la información que especifique. Por ejemplo, si escribe XNS o TCP, la función genera una ruta de acceso a Xns.ini o Tcp.ini, respectivamente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                            |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl>   |
| Biblioteca<br/>                  | <dl> <dt>Parser.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl>  |



 

 




