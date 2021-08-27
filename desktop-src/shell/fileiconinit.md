---
description: Inicializa o reinicializa la lista de imágenes del sistema.
ms.assetid: 4e661326-157e-4c75-86df-cd213e01c3e5
title: Función FileIconInit
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FileIconInit
api_type:
- DllExport
api_location:
- Shell32.dll
ms.openlocfilehash: 1771e1f0bde83f0fc7d070787b7a19f87007e26bd1ad42dcaa88e230e61a60af
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120111815"
---
# <a name="fileiconinit-function"></a>Función FileIconInit

Inicializa o reinicializa la lista de imágenes del sistema.

## <a name="syntax"></a>Sintaxis


```C++
BOOL FileIconInit(
  _In_ BOOL fRestoreCache
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*fRestoreCache* \[ En\]
</dt> <dd>

Tipo: **BOOL**

**TRUE** para restaurar la caché de imágenes del sistema desde el disco; **False en** caso contrario.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **BOOL**

**TRUE** si la memoria caché se actualizó correctamente, **FALSE** si se ha realizado un error en la inicialización.

## <a name="remarks"></a>Comentarios

Si usa listas de imágenes del sistema en su propio proceso, debe llamar a **FileIconInit** en las siguientes ocasiones:

-   Al iniciar.
-   En respuesta a un [**mensaje \_ WM SETTINGCHANGE**](../winmsg/wm-settingchange.md) cuando se establece la marca [**SPI \_ SETNONCLIENTMETRICS.**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa)

**FileIconInit** no se incluye en un archivo de encabezado. Debe llamarlo directamente desde Shell32.dll, mediante el ordinal 660.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>                                            |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                   |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll</dt> </dl> |



 

 
