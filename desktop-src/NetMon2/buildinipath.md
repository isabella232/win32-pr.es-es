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
ms.openlocfilehash: 3f715e740319515fe4772d1a9905a2f9b563f3cb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071567"
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

Nombre del archivo INI (el nombre de archivo completo menos la extensión de nombre de archivo).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es un puntero al nombre de archivo INI completo.

Si la función no se realiza correctamente, el valor devuelto es **NULL.**

## <a name="remarks"></a>Observaciones

La ruta de acceso que devuelve esta función es una ruta de acceso completa a un archivo INI que corresponde a la información que especifique. Por ejemplo, si escribe XNS o TCP, la función genera una ruta de acceso para Xns.ini o Tcp.ini, respectivamente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                            |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl>   |
| Biblioteca<br/>                  | <dl> <dt>Parser.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl>  |



 

 




