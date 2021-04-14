---
title: WMDRM_IMPORT_CONTENT_KEY estructura (Drmexternals. h)
description: La \_ estructura de clave de contenido de importación de WMDRM \_ \_ almacena la clave de contenido que se usa en la importación de contenido protegido.
ms.assetid: 29a0f98d-96a3-46b2-a67c-dbb23449e927
keywords:
- WMDRM_IMPORT_CONTENT_KEY estructura de Windows Media Format
- Formato de Windows Media de estructura
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
ms.openlocfilehash: d616cfe856a19f4f8ffa5254254d3946b1544dc6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104421979"
---
# <a name="wmdrm_import_content_key-structure"></a>\_Estructura de \_ clave de contenido de importación de WMDRM \_

La estructura de clave de contenido de importación de WMDRM almacena la clave de contenido que se usa en la importación de contenido protegido. **\_ \_ \_**

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

Tipo de clave de contenido. Establezca en el valor de cóctel del KEYTYPE de WMDRM \_ \_ .

</dd> <dt>

**cbContentKey**
</dt> <dd>

Tamaño de la clave de contenido en bytes.

</dd> <dt>

**rgbKeyData**
</dt> <dd>

Dirección de un búfer que contiene la clave de contenido. El tamaño del búfer debe coincidir con el valor de **cbContentKey**. Esta clave debe coincidir con la clave importada del mensaje de licencia de XMR.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Esta estructura, incluido el búfer que contiene la clave de sesión, se debe cifrar con la clave de sesión e incluirse en el miembro **pbEncryptedKeyMessage** de la estructura de la estructura de la estructura de [**importación de WMDRM \_ \_ \_**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmdrm_import_init_struct) .

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

 

 





