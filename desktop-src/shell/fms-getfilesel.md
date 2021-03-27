---
description: Contiene información sobre un archivo seleccionado en la ventana del administrador de archivos activo (la ventana Directorio o la ventana Resultados de la búsqueda).
title: FMS_GETFILESEL estructura (Wfext. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMS_GETFILESEL
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: d8339f87-ba05-40bf-b7d1-a9de29eb15a4
ms.openlocfilehash: e7ae92350e88e050b1208eed6e08f8faba811fee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000858"
---
# <a name="fms_getfilesel-structure"></a>Estructura de FMS \_ GETFILESEL

Contiene información sobre un archivo seleccionado en la ventana del administrador de archivos activo (la ventana Directorio o la ventana Resultados de la búsqueda).

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _FMS_GETFILESEL {
  FILETIME ftTime;
  DWORD    dwSize;
  BYTE     bAttr;
  TCHAR    szName;
} FMS_GETFILESEL;
```



## <a name="members"></a>Miembros

<dl> <dt>

**ftTime**
</dt> <dd>

Tipo: **FILETIME**

</dd> <dd>

Fecha y hora en que se creó el archivo.

</dd> <dt>

**dwSize**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Tamaño, en bytes, del archivo.

</dd> <dt>

**Bater**
</dt> <dd>

Tipo: **byte**

</dd> <dd>

Atributos del archivo.

</dd> <dt>

**szName**
</dt> <dd>

Tipo: **TCHAR**

</dd> <dd>

La ruta de acceso completa y el nombre de archivo del archivo seleccionado terminados en NULL.

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
</dt> </dl>

 

 




