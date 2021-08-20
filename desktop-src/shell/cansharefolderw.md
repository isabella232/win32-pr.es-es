---
description: Se usa para determinar si se va a mostrar la opción Compartir esta carpeta en la vista web.
title: Función CanShareFolderW
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CanShareFolderW
- CanShareFolderW
api_type:
- DllExport
api_location:
- Ntshrui.dll
ms.assetid: 5fd28a14-53e7-4016-9c49-9bb14ce7808b
ms.openlocfilehash: 7013c6ae825c34ae7d2dd7b9d507eac1e52c8d4e3a27182e5297e72ef13b4d9f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119032873"
---
# <a name="cansharefolderw-function"></a>Función CanShareFolderW

\[Esta función está disponible a través Windows XP con Service Pack 2 (SP2) y Windows Server 2003. Podría modificarse o no estar disponible en versiones posteriores de Windows.\]

Se usa para determinar si se va a mostrar la **opción Compartir esta** carpeta en la vista web.

## <a name="syntax"></a>Sintaxis


```C++
STDAPI CanShareFolderW(
  _In_ LPCWSTR pszPath
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pszPath* \[ En\]
</dt> <dd>

Tipo: **LPCWSTR**

Puntero a una cadena que especifica la ruta de acceso de la carpeta que se probará.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **STDAPI**

Los valores devueltos incluyen lo siguiente.



| Código o valor devuelto                                                                        | Descripción                                                                           |
|------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>     | La ruta de acceso a la *que apunta pszPath* especifica una carpeta que se puede compartir.<br/>    |
| <dl> <dt>**S \_ FALSE**</dt> </dl>  | La ruta de acceso a la *que apunta pszPath* especifica una carpeta que no se puede compartir.<br/> |
| <dl> <dt>Error HRESULT</dt> </dl> | Se ha producido un error.<br/>                                                     |



 

## <a name="remarks"></a>Comentarios

Esta función no tiene ningún archivo .lib asociado. Debe usar [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para usarlo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>                                            |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                   |
| Archivo DLL<br/>                      | <dl> <dt>Ntshrui.dll</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **CanShareFolderW** (Unicode)<br/>                                               |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ShowShareFolderUI**](./showsharefolderui.md)
</dt> </dl>

 

 
