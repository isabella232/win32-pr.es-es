---
description: Anula el registro de una clase de ventana registrada por LinkWindow \_ RegisterClass.
ms.assetid: 9e5c4326-efd1-43ca-a087-a436fe3f9bbd
title: LinkWindow_UnregisterClass función
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LinkWindow_UnregisterClass
api_type:
- DllExport
api_location:
- Shell32.dll
ms.openlocfilehash: 05a50d5f3af72c31ee04a1a9e8264acb22327c38f79f765ce2ad7a740086747e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118968944"
---
# <a name="linkwindow_unregisterclass-function"></a>Función LinkWindow \_ UnregisterClass

\[Esta función está disponible a través Windows XP con Service Pack 2 (SP2) y Windows Server 2003. Podría modificarse o no estar disponible en versiones posteriores de Windows.\]

Anula el registro de una clase de ventana registrada [**por LinkWindow \_ RegisterClass**](linkwindow-registerclass.md).

## <a name="syntax"></a>Sintaxis


```C++
BOOL LinkWindow_UnregisterClass(void);
```



## <a name="parameters"></a>Parámetros

Esta función no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Tipo: **BOOL**

Devuelve **TRUE** si la operación se ha realizado correctamente; **FALSE en** caso contrario.

## <a name="remarks"></a>Comentarios

Esta función no tiene un archivo de encabezado o biblioteca asociado, por lo que debe llamarse mediante un valor ordinal. Llame [**a LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) con el nombre dll Shell32.dll para obtener un identificador de módulo. A [**continuación, llame a GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) con ese identificador de módulo y el número ordinal 259 para usar esta función.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                    |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                          |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll (versión 5.0 o posterior)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Información general de los controles SysLink](../controls/syslink-overview.md)
</dt> </dl>

 

 
