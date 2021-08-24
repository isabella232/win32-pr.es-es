---
title: WMDRM_ENCRYPT_SCATTER_BLOCK estructura (Wmdrmsdk.h)
description: La estructura WMDRM \_ ENCRYPT SCATTER BLOCK contiene un bloque de datos que se va a \_ \_ cifrar.
ms.assetid: 73c871f0-3d0d-480f-856c-0f7d5dde5895
keywords:
- WMDRM_ENCRYPT_SCATTER_BLOCK structure windows Media Format
- Estructura de windows Formato multimedia
topic_type:
- apiref
api_name:
- WMDRM_ENCRYPT_SCATTER_BLOCK
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 258cb7e0d8d2cac8da40197aaa45028a56af0ff3a313d65c1a98c50d45b8d3b0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119658165"
---
# <a name="wmdrm_encrypt_scatter_block-structure"></a>Estructura DE \_ BLOQUES DE DISPERSIÓN DE CIFRADO \_ DE WMDRM \_

La **estructura WMDRM \_ ENCRYPT SCATTER \_ \_ BLOCK** contiene un bloque de datos que se va a cifrar.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct WMDRM_ENCRYPT_SCATTER_BLOCK {
  DWORD dwStreamID;
  DWORD cbBlock;
  BYTE  *pbBlock;
} ;
```



## <a name="members"></a>Miembros

<dl> <dt>

**dwStreamID**
</dt> <dd>

Identificador del flujo al que pertenece el bloque de datos.

</dd> <dt>

**cbBlock**
</dt> <dd>

Tamaño del bloque en bytes.

</dd> <dt>

**pbBlock**
</dt> <dd>

Puntero a un búfer que contiene el bloque de datos.

</dd> </dl>

## <a name="remarks"></a>Comentarios

El método [**IWMDRMEncryptScatter::EncryptScatter**](iwmdrmencryptscatter-encryptscatter.md) usa esta estructura para identificar los bloques de datos que se cifran.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Wmdrmsdk.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Estructuras**](drm-structures.md)
</dt> </dl>

 

 





