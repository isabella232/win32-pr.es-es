---
description: Muestra la pestaña Uso compartido de carpetas en la hoja de propiedades de la carpeta especificada.
ms.assetid: e622e4bb-eaf7-494f-b2a2-78ba1311a496
title: Función ShowShareFolderUI
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShowShareFolderUI
- ShowShareFolderUIW
api_type:
- DllExport
api_location:
- Ntshrui.dll
ms.openlocfilehash: 9683d7faee4bd44bd8f21e14250503f351e1a134119f978f872d7a0fe3ad6c4b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118968264"
---
# <a name="showsharefolderui-function"></a>Función ShowShareFolderUI

Muestra la **pestaña Uso compartido de** carpetas en la hoja de propiedades de la carpeta especificada.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ShowShareFolderUI(
  _In_ HWND    hwndParent,
  _In_ LPCWSTR pszPath
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hwndParent* \[ En\]
</dt> <dd>

Tipo: **HWND**

Identificador de la ventana primaria de la hoja de propiedades.

</dd> <dt>

*pszPath* \[ En\]
</dt> <dd>

Tipo: **LPCWSTR**

Puntero a una cadena que especifica la ruta de acceso a la carpeta que muestra su **pestaña Uso compartido de** carpetas.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Esta función siempre devuelve S \_ OK.

## <a name="remarks"></a>Comentarios

Esta función no tiene ningún archivo .lib asociado. Debe usar [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para usarlo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                            |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                   |
| Archivo DLL<br/>                      | <dl> <dt>Ntshrui.dll</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **ShowShareFolderUIW** (Unicode)<br/>                                            |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CanShareFolderW**](cansharefolderw.md)
</dt> </dl>

 

 
