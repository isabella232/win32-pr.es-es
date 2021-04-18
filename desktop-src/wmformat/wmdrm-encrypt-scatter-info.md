---
title: WMDRM_ENCRYPT_SCATTER_INFO estructura (wmdrmsdk. h)
description: La \_ \_ \_ estructura de la información de dispersión cifrada de WMDRM contiene información necesaria para configurar la interfaz IWMDRMEncryptScatter para su uso.
ms.assetid: 25e19511-56ac-441b-b521-5097dd792ead
keywords:
- WMDRM_ENCRYPT_SCATTER_INFO estructura de Windows Media Format
- Formato de Windows Media de estructura
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
ms.openlocfilehash: 500012231f6860fd94038b240355eda9aa2aee44
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105721587"
---
# <a name="wmdrm_encrypt_scatter_info-structure"></a>\_Estructura de \_ información de dispersión cifrada de WMDRM \_

La estructura de la **\_ \_ \_ información de dispersión cifrada de WMDRM** contiene información necesaria para configurar la interfaz [**IWMDRMEncryptScatter**](iwmdrmencryptscatter.md) para su uso.

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

Versión de protección de ejemplo que se va a usar para codificar los datos de la secuencia especificada.

</dd> <dt>

**cbProtectionInfo**
</dt> <dd>

Tamaño del búfer de **pbProtectionInfo** en bytes.

</dd> <dt>

**pbProtectionInfo**
</dt> <dd>

Búfer que contiene información de protección adicional.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El método [**IWMDRMEncryptScatter:: InitEncryptScatter**](iwmdrmencryptscatter-initencryptscatter.md) usa esta estructura.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Estructuras**](drm-structures.md)
</dt> </dl>

 

 





