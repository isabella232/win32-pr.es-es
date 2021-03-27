---
description: Inicializa o reinicializa la lista de imágenes del sistema.
ms.assetid: 4e661326-157e-4c75-86df-cd213e01c3e5
title: FileIconInit función)
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
ms.openlocfilehash: 090f35cc576caf6f99a8d5822a0304f15383e8db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360682"
---
# <a name="fileiconinit-function"></a>FileIconInit función)

Inicializa o reinicializa la lista de imágenes del sistema.

## <a name="syntax"></a>Sintaxis


```C++
BOOL FileIconInit(
  _In_ BOOL fRestoreCache
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*fRestoreCache* \[ de\]
</dt> <dd>

Tipo: **bool**

**True** para restaurar la memoria caché de la imagen del sistema desde el disco; De lo contrario, **false** .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **bool**

**True** si la memoria caché se actualizó correctamente, **false** si se produjo un error en la inicialización.

## <a name="remarks"></a>Observaciones

Si usa listas de imágenes del sistema en su propio proceso, debe llamar a **FileIconInit** en los momentos siguientes:

-   Al iniciar.
-   En respuesta a un mensaje de [**\_ SETTINGCHANGE de WM**](../winmsg/wm-settingchange.md) cuando se establece la marca [**SPI \_ SETNONCLIENTMETRICS**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) .

**FileIconInit** no se incluye en un archivo de encabezado. Debe llamarlo directamente desde Shell32.dll, utilizando el ordinal 660.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                            |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                   |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll</dt> </dl> |



 

 
