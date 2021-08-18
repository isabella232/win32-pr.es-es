---
description: Vacía la memoria caché de la base de datos shim. Se debe llamar a esta función después de instalar una nueva base de datos shim.
ms.assetid: 7e5bbdca-7b58-4c51-9cd1-105b05ee7fbe
title: Función ShimFlushCache
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShimFlushCache
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: ecf1291b7fdcfb43170ec7e269fa140c321fafdbc09989fc7ee2b392f11c1160
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119075919"
---
# <a name="shimflushcache-function"></a>Función ShimFlushCache

Vacía la memoria caché de la base de datos shim. Se debe llamar a esta función después de instalar una nueva base de datos shim.

## <a name="syntax"></a>Sintaxis


```C++
BOOL WINAPI ShimFlushCache(
  _In_opt_ HWND      hwnd,
  _In_opt_ HINSTANCE hInstance,
  _In_opt_ LPCSTR    lpszCmdLine,
  _In_     int       nCmdShow
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hwnd* \[ in, opcional\]
</dt> <dd>

Sin usar; debe ser 0.

</dd> <dt>

*hInstance* \[ in, opcional\]
</dt> <dd>

Sin usar; debe ser 0.

</dd> <dt>

*lpszCmdLine* \[ in, opcional\]
</dt> <dd>

Sin usar; debe ser 0.

</dd> <dt>

*nCmdShow* \[ En\]
</dt> <dd>

Sin usar; debe ser 0.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

La función devuelve **TRUE si** se ejecuta correctamente o **FALSE** en caso de error.

## <a name="remarks"></a>Comentarios

El autor de la llamada debe ser un administrador.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                         |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                   |
| Archivo DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**BaseFlushAppcompatCache**](baseflushappcompatcache.md)
</dt> </dl>

 

 




