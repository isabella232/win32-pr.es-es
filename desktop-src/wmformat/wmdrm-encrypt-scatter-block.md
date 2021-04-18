---
title: WMDRM_ENCRYPT_SCATTER_BLOCK estructura (wmdrmsdk. h)
description: La \_ \_ \_ estructura de bloques de dispersión cifrada WMDRM contiene un bloque de datos que se van a cifrar.
ms.assetid: 73c871f0-3d0d-480f-856c-0f7d5dde5895
keywords:
- WMDRM_ENCRYPT_SCATTER_BLOCK estructura de Windows Media Format
- Formato de Windows Media de estructura
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
ms.openlocfilehash: 8911ba1822b146de4a99ff1fe144afcfd8e212e8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105721581"
---
# <a name="wmdrm_encrypt_scatter_block-structure"></a>\_Cifrado de la \_ estructura de bloques de dispersión de WMDRM \_

La estructura de **\_ \_ \_ bloques de dispersión cifrada WMDRM** contiene un bloque de datos que se van a cifrar.

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

Identificador de la secuencia a la que pertenece el bloque de datos.

</dd> <dt>

**cbBlock**
</dt> <dd>

Tamaño del bloque en bytes.

</dd> <dt>

**pbBlock**
</dt> <dd>

Puntero a un búfer que contiene el bloque de datos.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El método [**IWMDRMEncryptScatter:: EncryptScatter**](iwmdrmencryptscatter-encryptscatter.md) usa esta estructura para identificar los bloques de datos que se van a cifrar.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Estructuras**](drm-structures.md)
</dt> </dl>

 

 





