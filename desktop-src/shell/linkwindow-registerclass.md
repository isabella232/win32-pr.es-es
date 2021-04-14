---
description: Registra una clase de ventana que permite usar el control común SysLink en una ventana.
ms.assetid: 1e6dd741-81be-40bb-a8b5-d565f593c4e9
title: LinkWindow_RegisterClass función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LinkWindow_RegisterClass
api_type:
- DllExport
api_location:
- Shell32.dll
ms.openlocfilehash: 7b5bfd2e1a45ff3f65df7cf3d3cae41bf4926aaa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985671"
---
# <a name="linkwindow_registerclass-function"></a>LinkWindow \_ RegisterClass (función)

\[Esta función está disponible a través de Windows XP con Service Pack 2 (SP2) y Windows Server 2003. Podría modificarse o no estar disponible en versiones posteriores de Windows. Use [**InitCommonControlsEx**](/windows/win32/api/commctrl/nf-commctrl-initcommoncontrolsex) en su lugar.\]

Registra una clase de ventana que permite usar el control común [SysLink](../controls/syslink-overview.md) en una ventana.

## <a name="syntax"></a>Sintaxis


```C++
BOOL LinkWindow_RegisterClass(void);
```



## <a name="parameters"></a>Parámetros

Esta función no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Tipo: **bool**

Devuelve **true** si el registro se realizó correctamente; De lo contrario, **false** .

## <a name="remarks"></a>Observaciones

Esta función no tiene un archivo de encabezado o biblioteca asociado, por lo que debe llamarse por valor ordinal. Llame a [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) con el nombre de dll Shell32.dll para obtener un identificador de módulo. A continuación, llame a [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) con ese identificador de módulo y el número ordinal 258 para usar esta función.

Use [**LinkWindow \_ UnregisterClass**](linkwindow-unregisterclass.md) para anular el registro de la clase después del uso.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                    |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                          |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll (versión 5,0 o posterior)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Información general sobre los controles SysLink](../controls/syslink-overview.md)
</dt> </dl>

 

 
