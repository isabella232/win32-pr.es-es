---
description: Contiene información acerca de la unidad seleccionada en la ventana del administrador de archivos activo (la ventana Directorio o la ventana Resultados de la búsqueda).
title: FMS_GETDRIVEINFO estructura (Wfext. h)
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
ms.openlocfilehash: b19b54d89f74fa122effa5853beb2961e0ddf1eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985510"
---
# <a name="fms_getdriveinfo-structure"></a>Estructura de FMS \_ GETDRIVEINFO

Contiene información acerca de la unidad seleccionada en la ventana del administrador de archivos activo (la ventana Directorio o la ventana Resultados de la búsqueda).

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



## <a name="members"></a>Miembros

<dl> <dt>

**dwTotalSpace**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

La cantidad total de espacio de almacenamiento, en bytes, del disco asociado a la unidad.

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

Etiqueta de volumen terminada en NULL del disco asociado a la unidad.

</dd> <dt>

**szShare**
</dt> <dd>

Tipo: **TCHAR \[ 128 \]**

</dd> <dd>

Nombre terminado en NULL del recurso de red (si se tiene acceso a la unidad a través de una red).

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                         |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Wfext. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**FMExtensionProc**](fmextensionproc.md)
</dt> <dt>

[**\_GETDRIVEINFO FM**](fm-getdriveinfo.md)
</dt> </dl>

 

 




