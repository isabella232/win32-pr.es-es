---
description: Vacía la caché de la base de datos de correcciones de compatibilidad. Se debe llamar a esta función después de instalar una nueva base de datos de correcciones de compatibilidad.
ms.assetid: 7e5bbdca-7b58-4c51-9cd1-105b05ee7fbe
title: ShimFlushCache función)
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
ms.openlocfilehash: 35e279c5036142ec87c5bad6d7c512388033bc94
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080086"
---
# <a name="shimflushcache-function"></a>ShimFlushCache función)

Vacía la caché de la base de datos de correcciones de compatibilidad. Se debe llamar a esta función después de instalar una nueva base de datos de correcciones de compatibilidad.

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

*hWnd* \[ en, opcional\]
</dt> <dd>

Sin usar debe ser 0.

</dd> <dt>

*hInstance* \[ en, opcional\]
</dt> <dd>

Sin usar debe ser 0.

</dd> <dt>

*lpszCmdLine* \[ en, opcional\]
</dt> <dd>

Sin usar debe ser 0.

</dd> <dt>

*nCmdShow* \[ de\]
</dt> <dd>

Sin usar debe ser 0.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

La función devuelve **true** si se ejecuta correctamente o **false** en caso de error.

## <a name="remarks"></a>Observaciones

El autor de la llamada debe ser un administrador.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                         |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                   |
| Archivo DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**BaseFlushAppcompatCache**](baseflushappcompatcache.md)
</dt> </dl>

 

 




