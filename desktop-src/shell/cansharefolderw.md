---
description: Se usa para determinar si se debe mostrar la opción compartir esta carpeta en la vista Web.
title: CanShareFolderW función)
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
ms.openlocfilehash: cf7d0feb31666f3a918c0307a0b0983bff246fea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540563"
---
# <a name="cansharefolderw-function"></a>CanShareFolderW función)

\[Esta función está disponible a través de Windows XP con Service Pack 2 (SP2) y Windows Server 2003. Podría modificarse o no estar disponible en versiones posteriores de Windows.\]

Se usa para determinar si se debe mostrar la opción **compartir esta carpeta en la** vista Web.

## <a name="syntax"></a>Sintaxis


```C++
STDAPI CanShareFolderW(
  _In_ LPCWSTR pszPath
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pszPath* \[ de\]
</dt> <dd>

Tipo: **LPCWSTR**

Puntero a una cadena que especifica la ruta de acceso de la carpeta que se va a probar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **STDAPI**

Los valores devueltos son los siguientes.



| Código o valor devuelto                                                                        | Descripción                                                                           |
|------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>     | La ruta de acceso a la que apunta *pszPath* especifica una carpeta que se puede compartir.<br/>    |
| <dl> <dt>**S \_ false**</dt> </dl>  | La ruta de acceso a la que apunta *pszPath* especifica una carpeta que no se puede compartir.<br/> |
| <dl> <dt>Error HRESULT</dt> </dl> | Se ha producido un error.<br/>                                                     |



 

## <a name="remarks"></a>Observaciones

Esta función no tiene ningún archivo. lib asociado. Debe utilizar [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para usarlo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                            |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                   |
| Archivo DLL<br/>                      | <dl> <dt>Ntshrui.dll</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **CanShareFolderW** (Unicode)<br/>                                               |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ShowShareFolderUI**](./showsharefolderui.md)
</dt> </dl>

 

 
