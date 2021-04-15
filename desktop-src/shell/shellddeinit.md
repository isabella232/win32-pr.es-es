---
description: Registra los servicios de Intercambio dinámico de datos de Shell (DDE) en el proceso actual, notificando al sistema que el proceso actual desea hospedar objetos DDE.
ms.assetid: d7f65d6a-a697-475b-a739-c7950b7f4d5d
title: ShellDDEInit función)
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
ms.openlocfilehash: cb2f4639d97a99cd063f372e303fd48b7a1d6e4d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985882"
---
# <a name="shellddeinit-function"></a>ShellDDEInit función)

Registra los servicios de Intercambio dinámico de datos de Shell (DDE) en el proceso actual, notificando al sistema que el proceso actual desea hospedar objetos DDE.

## <a name="syntax"></a>Sintaxis


```C++
void ShellDDEInit(
  _In_ BOOL init
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*init* \[ de\]
</dt> <dd>

Tipo: **bool**

**True** para registrar el proceso actual como host DDE; **False** para anular el registro.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

El proceso que llama a esta función actúa como el Shell y se usa para ver el contenido de las carpetas abiertas con el verbo ' Open ' de [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) .

Esta función no tiene un archivo de encabezado o biblioteca asociado, por lo que debe llamarse por valor ordinal. Llame a [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) con el nombre del archivo DLL (Shdocvw.dll) para obtener un identificador de módulo. A continuación, llame a [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) con ese identificador de módulo y el número ordinal de función 118 para obtener la dirección de la función.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP, Windows 2000 Professional \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                          |
| Archivo DLL<br/>                      | <dl> <dt>Shdocvw.dll (versión 6,0 o posterior)</dt> </dl> |



 

 
