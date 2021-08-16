---
description: Registra una clase de ventana que permite usar el control común SysLink en una ventana.
ms.assetid: 1e6dd741-81be-40bb-a8b5-d565f593c4e9
title: LinkWindow_RegisterClass función
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
ms.openlocfilehash: 75936c918a930698ef803b02743b935660e876b0d87d7f6d5eddce91d4f4c0a5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118968964"
---
# <a name="linkwindow_registerclass-function"></a>Función LinkWindow \_ RegisterClass

\[Esta función está disponible a través Windows XP con Service Pack 2 (SP2) y Windows Server 2003. Podría modificarse o no estar disponible en versiones posteriores de Windows. Use [**InitCommonControlsEx en**](/windows/win32/api/commctrl/nf-commctrl-initcommoncontrolsex) su lugar.\]

Registra una clase de ventana que permite usar el control [común SysLink](../controls/syslink-overview.md) en una ventana.

## <a name="syntax"></a>Sintaxis


```C++
BOOL LinkWindow_RegisterClass(void);
```



## <a name="parameters"></a>Parámetros

Esta función no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Tipo: **BOOL**

Devuelve **TRUE si** el registro se ha realizado correctamente; **FALSE en** caso contrario.

## <a name="remarks"></a>Comentarios

Esta función no tiene un archivo de encabezado o biblioteca asociado, por lo que debe llamarse mediante un valor ordinal. Llame [**a LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) con el nombre dll Shell32.dll para obtener un identificador de módulo. A [**continuación, llame a GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) con ese identificador de módulo y el número ordinal 258 para usar esta función.

Use [**LinkWindow \_ UnregisterClass para**](linkwindow-unregisterclass.md) anular el registro de la clase después de su uso.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                    |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                          |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll (versión 5.0 o posterior)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Información general de los controles SysLink](../controls/syslink-overview.md)
</dt> </dl>

 

 
