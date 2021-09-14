---
title: DRM_PLAYLIST_CONTENT_ID estructura (Drmexternals.h)
description: La estructura DEL IDENTIFICADOR DE CONTENIDO DE LA LISTA DE REPRODUCCIÓN DE DRM contiene información sobre el contenido que se va a copiar en CD como \_ parte de una grabación de lista de \_ \_ reproducción.
ms.assetid: 124e86ac-b0d4-40b2-868b-fe2fed1898e1
keywords:
- DRM_PLAYLIST_CONTENT_ID structure windows Media Format
- Estructura de windows Formato multimedia
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359925"
---
# <a name="drm_playlist_content_id-structure"></a>Estructura del \_ IDENTIFICADOR DE CONTENIDO DE LA LISTA DE REPRODUCCIÓN \_ \_ DE DRM

La **estructura DEL IDENTIFICADOR DE CONTENIDO DE LA \_ \_ \_ LISTA** DE REPRODUCCIÓN DE DRM contiene información sobre el contenido que se va a copiar en CD como parte de una grabación de lista de reproducción.

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



## <a name="members"></a>Members

<dl> <dt>

**lpcwszV2Header**
</dt> <dd>

Encabezado DRM. Use este miembro si el contenido está protegido por Windows DRM multimedia versión 2 o posterior.

</dd> <dt>

**lpcszV1KID**
</dt> <dd>

El identificador de la clave. Use este miembro si el contenido está protegido por Windows DRM multimedia versión 1.

</dd> <dt>

**pbOtherData**
</dt> <dd>

Búfer que contiene datos adicionales.

</dd> <dt>

**cbOtherData**
</dt> <dd>

Tamaño del búfer **pbOtherData** en bytes.

</dd> <dt>

**dwUniqueIDForSession**
</dt> <dd>

Identificador único del contenido que se va a usar en la sesión actual.

</dd> <dt>

**dwValidFields**
</dt> <dd>

**DWORD** que indica los campos válidos de esta estructura.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                               |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                      |
| Versión<br/>                  | Windows SDK de formato multimedia 11<br/>                                                    |
| Encabezado<br/>                   | <dl> <dt>Drmexternals.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Estructuras**](structures.md)
</dt> </dl>

 

 





