---
description: Contiene información sobre un archivo seleccionado en la ventana activa del Administrador de archivos (la ventana de directorio o la ventana Resultados de la búsqueda).
title: FMS_GETFILESEL estructura (Wfext.h)
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
ms.openlocfilehash: b1188840299a101081c5c29d0e5658963ca7a72e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127257066"
---
# <a name="fms_getfilesel-structure"></a>FMS \_ GETFILESEL (estructura)

Contiene información sobre un archivo seleccionado en la ventana activa del Administrador de archivos (la ventana de directorio o la ventana Resultados de la búsqueda).

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _FMS_GETFILESEL {
  FILETIME ftTime;
  DWORD    dwSize;
  BYTE     bAttr;
  TCHAR    szName;
} FMS_GETFILESEL;
```



## <a name="members"></a>Members

<dl> <dt>

**ftTime**
</dt> <dd>

Tipo: **FILETIME**

</dd> <dd>

La hora y la fecha en que se creó el archivo.

</dd> <dt>

**dwSize**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Tamaño, en bytes, del archivo.

</dd> <dt>

**bAttr**
</dt> <dd>

Tipo: **BYTE**

</dd> <dd>

Atributos del archivo.

</dd> <dt>

**szName**
</dt> <dd>

Tipo: **TCHAR**

</dd> <dd>

Ruta de acceso completa terminada en NULL y nombre de archivo del archivo seleccionado.

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
</dt> </dl>

 

 




