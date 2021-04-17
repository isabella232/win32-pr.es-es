---
title: DRM_PLAYLIST_CONTENT_ID estructura (Drmexternals. h)
description: La \_ estructura de \_ ID. de contenido de la lista de reproducción DRM \_ contiene información sobre el contenido que se va a copiar en el CD como parte de la grabación de una lista de reproducción.
ms.assetid: 124e86ac-b0d4-40b2-868b-fe2fed1898e1
keywords:
- DRM_PLAYLIST_CONTENT_ID estructura de Windows Media Format
- Formato de Windows Media de estructura
topic_type:
- apiref
api_name:
- DRM_PLAYLIST_CONTENT_ID
api_location:
- Drmexternals.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f475a8c3620ff1af64cb70914ca1ac591aa55106
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105705160"
---
# <a name="drm_playlist_content_id-structure"></a>\_Estructura de \_ \_ ID. de contenido de lista de reproducción DRM

La estructura de **\_ \_ \_ ID. de contenido de la lista de reproducción DRM** contiene información sobre el contenido que se va a copiar en el CD como parte de la grabación de una lista de reproducción.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct DRM_PLAYLIST_CONTENT_ID {
  LPCWSTR lpcwszV2Header;
  LPCSTR  lpcszV1KID;
  BYTE    *pbOtherData;
  DWORD   cbOtherData;
  DWORD   dwUniqueIDForSession;
  DWORD   dwValidFields;
} ;
```



## <a name="members"></a>Miembros

<dl> <dt>

**lpcwszV2Header**
</dt> <dd>

Encabezado DRM. Utilice este miembro si el contenido está protegido por la versión 2 o posterior de DRM de Windows Media.

</dd> <dt>

**lpcszV1KID**
</dt> <dd>

El identificador de la clave. Utilice este miembro si el contenido está protegido por la versión 1 de DRM de Windows Media.

</dd> <dt>

**pbOtherData**
</dt> <dd>

Búfer que contiene datos complementarios.

</dd> <dt>

**cbOtherData**
</dt> <dd>

Tamaño del búfer de **pbOtherData** en bytes.

</dd> <dt>

**dwUniqueIDForSession**
</dt> <dd>

Identificador único para el contenido que se va a usar en la sesión actual.

</dd> <dt>

**dwValidFields**
</dt> <dd>

**DWORD** que indica los campos válidos de esta estructura.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                               |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                      |
| Versión<br/>                  | SDK de Windows Media Format 11<br/>                                                    |
| Encabezado<br/>                   | <dl> <dt>Drmexternals. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Estructuras**](structures.md)
</dt> </dl>

 

 





