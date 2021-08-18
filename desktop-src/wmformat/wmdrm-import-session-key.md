---
title: WMDRM_IMPORT_SESSION_KEY estructura (Drmexternals.h)
description: La estructura WMDRM \_ IMPORT SESSION KEY contiene la clave de sesión para importar contenido \_ \_ protegido.
ms.assetid: 2dd1e8ec-a25f-4ced-8f1b-286534c66ebf
keywords:
- WMDRM_IMPORT_SESSION_KEY structure windows Media Format
- Estructura de windows Formato multimedia
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
ms.openlocfilehash: d34cdff6d17ad6ce60dd40478b56c9718be0863295422d2e5c60fee2c437dc6f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117844064"
---
# <a name="wmdrm_import_session_key-structure"></a>Estructura DE CLAVE \_ DE SESIÓN DE IMPORTACIÓN \_ DE WMDRM \_

La **estructura WMDRM \_ IMPORT SESSION \_ \_ KEY** contiene la clave de sesión para importar contenido protegido.

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

Tamaño de la clave de sesión, en bytes. Este valor puede ser tan grande como necesite, dados los límites de una única operación OAEP rsa en todo el mensaje (esta estructura más la clave de sesión).

</dd> <dt>

**rgbKey**
</dt> <dd>

Dirección de un búfer que contiene la clave de sesión. El tamaño del búfer debe coincidir con el valor **de cbKey**. Los datos del búfer son un valor de clave generado aleatoriamente.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Esta estructura, incluido el búfer que contiene la clave de sesión, debe cifrarse con la clave pública de máquina DRM de medios de Windows e incluirse en el miembro **pbEncryptedSessionKeyMessage** de la estructura [**\_ \_ \_ STRUCT WMDRM IMPORT INIT.**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmdrm_import_init_struct)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                               |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                      |
| Versión<br/>                  | Windows SDK de formato multimedia 11<br/>                                                    |
| Header<br/>                   | <dl> <dt>Drmexternals.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Estructuras**](structures.md)
</dt> </dl>

 

 





