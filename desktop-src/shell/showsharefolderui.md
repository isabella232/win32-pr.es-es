---
description: Muestra la ficha compartir carpetas de la hoja de propiedades de la carpeta especificada.
ms.assetid: e622e4bb-eaf7-494f-b2a2-78ba1311a496
title: ShowShareFolderUI función)
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
ms.openlocfilehash: e6270f72d1574a21b98ac9ee3151af1f34f08a72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104360884"
---
# <a name="showsharefolderui-function"></a>ShowShareFolderUI función)

Muestra la ficha **compartir carpetas** de la hoja de propiedades de la carpeta especificada.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ShowShareFolderUI(
  _In_ HWND    hwndParent,
  _In_ LPCWSTR pszPath
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hwndParent* \[ de\]
</dt> <dd>

Tipo: **hWnd**

Identificador de la ventana primaria de la hoja de propiedades.

</dd> <dt>

*pszPath* \[ de\]
</dt> <dd>

Tipo: **LPCWSTR**

Un puntero a una cadena que especifica la ruta de acceso a la carpeta que muestra su ficha de **uso compartido de carpetas** .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Esta función siempre devuelve S \_ correcto.

## <a name="remarks"></a>Observaciones

Esta función no tiene ningún archivo. lib asociado. Debe utilizar [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para usarlo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                            |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                   |
| Archivo DLL<br/>                      | <dl> <dt>Ntshrui.dll</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **ShowShareFolderUIW** (Unicode)<br/>                                            |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CanShareFolderW**](cansharefolderw.md)
</dt> </dl>

 

 
