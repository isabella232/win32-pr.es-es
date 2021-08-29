---
title: WMDRM_IMPORT_CONTENT_KEY estructura (Drmexternals.h)
description: La estructura WMDRM IMPORT CONTENT KEY almacena la clave de contenido que se usa \_ \_ para importar contenido \_ protegido.
ms.assetid: 29a0f98d-96a3-46b2-a67c-dbb23449e927
keywords:
- WMDRM_IMPORT_CONTENT_KEY structure windows Media Format
- Estructura de windows Formato multimedia
topic_type:
- apiref
api_name:
- WMDRM_IMPORT_CONTENT_KEY
api_location:
- Drmexternals.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7f7ced03d841d71e104384fff3f7abdfdd13890746f8052cf43264dacd22c03
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119083799"
---
# <a name="wmdrm_import_content_key-structure"></a>Estructura DE CLAVE DE \_ \_ CONTENIDO DE IMPORTACIÓN DE WMDRM \_

La **estructura WMDRM \_ IMPORT CONTENT \_ \_ KEY** almacena la clave de contenido que se usa para importar contenido protegido.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct WMDRM_IMPORT_CONTENT_KEY {
  DWORD dwVersion;
  DWORD cbStructSize;
  DWORD dwIVKeyType;
  DWORD cbIVKey;
  DWORD dwContentKeyType;
  DWORD cbContentKey;
  BYTE  rgbKeyData[1];
} ;
```



## <a name="members"></a>Miembros

<dl> <dt>

**dwVersion**
</dt> <dd>

Se trata de la versión.

</dd> <dt>

**cbStructSize**
</dt> <dd>

Tamaño de la estructura en bytes.

</dd> <dt>

**dwIVKeyType**
</dt> <dd>

Tipo de clave de vector de inicialización. Establezca en WMDRM \_ KEYTYPE \_ RC4.

</dd> <dt>

**cbIVKey**
</dt> <dd>

Tamaño de la clave de vector de inicialización en bytes.

</dd> <dt>

**dwContentKeyType**
</dt> <dd>

Tipo de clave de contenido. Se establece en WMDRM \_ KEYTYPE \_ WM.

</dd> <dt>

**cbContentKey**
</dt> <dd>

Tamaño de la clave de contenido en bytes.

</dd> <dt>

**rgbKeyData**
</dt> <dd>

Dirección de un búfer que contiene la clave de contenido. El tamaño del búfer debe coincidir con el valor **de cbContentKey.** Esta clave debe coincidir con la clave importada desde el mensaje de licencia de XMR.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Esta estructura, incluido el búfer que contiene la clave de sesión, debe cifrarse con la clave de sesión e incluirse en el **miembro pbEncryptedKeyMessage** de la estructura [**STRUCT DE WMDRM \_ IMPORT \_ INIT. \_**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmdrm_import_init_struct)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                               |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                      |
| Versión<br/>                  | Windows SDK de formato multimedia 11<br/>                                                    |
| Header<br/>                   | <dl> <dt>Drmexternals.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Estructuras**](structures.md)
</dt> </dl>

 

 





