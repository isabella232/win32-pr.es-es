---
title: WMDRM_IMPORT_SESSION_KEY estructura (Drmexternals. h)
description: La \_ \_ \_ estructura de la clave de sesión de importación de WMDRM contiene la clave de sesión para importar contenido protegido.
ms.assetid: 2dd1e8ec-a25f-4ced-8f1b-286534c66ebf
keywords:
- WMDRM_IMPORT_SESSION_KEY estructura de Windows Media Format
- Formato de Windows Media de estructura
topic_type:
- apiref
api_name:
- WMDRM_IMPORT_SESSION_KEY
api_location:
- Drmexternals.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 93295e73e4e3e5e13b438f8b62e0ab6bfff43ee7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150827"
---
# <a name="wmdrm_import_session_key-structure"></a>\_Estructura de \_ claves de sesión de importación de WMDRM \_

La estructura de la clave de sesión de importación de WMDRM contiene la clave de sesión para importar contenido protegido. **\_ \_ \_**

## <a name="syntax"></a>Sintaxis


```C++
typedef struct WMDRM_IMPORT_SESSION_KEY {
  DWORD dwKeyType;
  DWORD cbKey;
  BYTE  rgbKey[1];
} ;
```



## <a name="members"></a>Miembros

<dl> <dt>

**dwKeyType**
</dt> <dd>

Tipo de clave de sesión. Establezca en WMDRM \_ KEYTYPE \_ RC4.

</dd> <dt>

**cbKey**
</dt> <dd>

Tamaño de la clave de sesión, en bytes. Este valor puede ser tan grande como sea necesario, dados los límites de una única operación de RSA OAEP en todo el mensaje (esta estructura más la clave de sesión).

</dd> <dt>

**rgbKey**
</dt> <dd>

Dirección de un búfer que contiene la clave de sesión. El tamaño del búfer debe coincidir con el valor de **cbKey**. Los datos del búfer son un valor de clave generado aleatoriamente.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Esta estructura, incluido el búfer que contiene la clave de sesión, se debe cifrar con la clave pública de la máquina DRM de Windows Media e incluirse en el miembro **pbEncryptedSessionKeyMessage** de la estructura de la estructura de [**\_ \_ inicialización \_ de la importación WMDRM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmdrm_import_init_struct) .

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

 

 





