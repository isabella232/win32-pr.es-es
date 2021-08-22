---
title: WMDRM_ENCRYPT_SCATTER_INFO estructura (Wmdrmsdk.h)
description: La estructura WMDRM ENCRYPT SCATTER INFO contiene información necesaria para configurar la \_ \_ interfaz \_ IWMDRMEncryptScatter para su uso.
ms.assetid: 25e19511-56ac-441b-b521-5097dd792ead
keywords:
- WMDRM_ENCRYPT_SCATTER_INFO windows Media Format de estructura
- estructura windows Formato multimedia
topic_type:
- apiref
api_name:
- WMDRM_ENCRYPT_SCATTER_INFO
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ef766f40742713b01648348bedb4c1a35494fdc02d02843f8f2a41f133938a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119083819"
---
# <a name="wmdrm_encrypt_scatter_info-structure"></a>Estructura DE INFORMACIÓN DE \_ DISPERSIÓN DE WMDRM ENCRYPT \_ \_

La **estructura WMDRM \_ ENCRYPT SCATTER \_ \_ INFO** contiene información necesaria para configurar la [**interfaz IWMDRMEncryptScatter**](iwmdrmencryptscatter.md) para su uso.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct WMDRM_ENCRYPT_SCATTER_INFO {
  DWORD dwStreamID;
  DWORD dwSampleProtectionVersion;
  DWORD cbProtectionInfo;
  BYTE  *pbProtectionInfo;
} ;
```



## <a name="members"></a>Miembros

<dl> <dt>

**dwStreamID**
</dt> <dd>

Identificador de la secuencia que se va a cifrar.

</dd> <dt>

**dwSampleProtectionVersion**
</dt> <dd>

Versión de protección de ejemplo que se usará para codificar datos de la secuencia especificada.

</dd> <dt>

**cbProtectionInfo**
</dt> <dd>

Tamaño del búfer **pbProtectionInfo** en bytes.

</dd> <dt>

**pbProtectionInfo**
</dt> <dd>

Búfer que contiene información de protección adicional.

</dd> </dl>

## <a name="remarks"></a>Comentarios

El método [**IWMDRMEncryptScatter::InitEncryptScatter**](iwmdrmencryptscatter-initencryptscatter.md) usa esta estructura.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Wmdrmsdk.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Estructuras**](drm-structures.md)
</dt> </dl>

 

 





