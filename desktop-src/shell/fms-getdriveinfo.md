---
description: Contiene información sobre la unidad seleccionada en la ventana activa del Administrador de archivos (la ventana de directorio o la ventana Resultados de la búsqueda).
title: FMS_GETDRIVEINFO estructura (Wfext.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMS_GETDRIVEINFO
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 14f8a90b-d0ed-4818-a719-8fc4ea617bef
ms.openlocfilehash: 107e12e1076a2fc928ecb9b578ab01d64898a83a
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842236"
---
# <a name="fms_getdriveinfo-structure"></a>FMS \_ GETDRIVEINFO (estructura)

Contiene información sobre la unidad seleccionada en la ventana activa del Administrador de archivos (la ventana de directorio o la ventana Resultados de la búsqueda).

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _FMS_GETDRIVEINFO {
  DWORD dwTotalSpace;
  DWORD dwFreeSpace;
  TCHAR szPath[260];
  TCHAR szVolume[14];
  TCHAR szShare[128];
} FMS_GETDRIVEINFO;
```



## <a name="members"></a>Members

<dl> <dt>

**dwTotalSpace**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Cantidad total de espacio de almacenamiento, en bytes, en el disco asociado a la unidad.

</dd> <dt>

**dwFreeSpace**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Cantidad de espacio de almacenamiento libre, en bytes, en el disco asociado a la unidad.

</dd> <dt>

**szPath**
</dt> <dd>

Tipo: **TCHAR \[ 260 \]**

</dd> <dd>

la ruta de acceso terminada en NULL del directorio actual.

</dd> <dt>

**szVolume**
</dt> <dd>

Tipo: **TCHAR \[ 14 \]**

</dd> <dd>

La etiqueta de volumen terminada en NULL del disco asociado a la unidad.

</dd> <dt>

**szShare**
</dt> <dd>

Tipo: **TCHAR \[ 128 \]**

</dd> <dd>

Nombre terminado en NULL del recurso de red (si se accede a la unidad a través de una red).

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                         |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Wfext.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**FMExtensionProc**](fmextensionproc.md)
</dt> <dt>

[**FM \_ GETDRIVEINFO**](fm-getdriveinfo.md)
</dt> </dl>

 

 




