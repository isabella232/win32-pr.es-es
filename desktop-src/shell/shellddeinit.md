---
description: Registra los servicios de datos dinámicos Exchange shell (DDE) en el proceso actual, notificando al sistema que el proceso actual desea hospedar objetos DDE.
ms.assetid: d7f65d6a-a697-475b-a739-c7950b7f4d5d
title: Función ShellDDEInit
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellDDEInit
api_type:
- DllExport
api_location:
- Shdocvw.dll
ms.openlocfilehash: 27d2e304cf3a67f522bbeec4835f5faa98b24d1509363873bb51387391f94b1b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117676717"
---
# <a name="shellddeinit-function"></a>Función ShellDDEInit

Registra los servicios de datos dinámicos Exchange shell (DDE) en el proceso actual, notificando al sistema que el proceso actual desea hospedar objetos DDE.

## <a name="syntax"></a>Sintaxis


```C++
void ShellDDEInit(
  _In_ BOOL init
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*init* \[ En\]
</dt> <dd>

Tipo: **BOOL**

**TRUE** para registrar el proceso actual como host DDE; **FALSE** para anular el registro.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

El proceso que llama a esta función actúa como shell y se usa para ver el contenido de las carpetas abiertas con el verbo "open" de [**ShellExecute.**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea)

Esta función no tiene un archivo de encabezado o biblioteca asociado, por lo que debe llamarse mediante un valor ordinal. Llame [**a LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) con el nombre dll (Shdocvw.dll) para obtener un identificador de módulo. A [**continuación, llame a GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) con ese identificador de módulo y el número ordinal 118 de la función para obtener la dirección de la función.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP, Windows 2000 Professional aplicaciones \[ de escritorio\]<br/>                                        |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                          |
| Archivo DLL<br/>                      | <dl> <dt>Shdocvw.dll (versión 6.0 o posterior)</dt> </dl> |



 

 
