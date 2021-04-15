---
title: Estructura de TSMF_SUPPORT_NODEDATA_IN
description: Se utiliza dentro de \_ los \_ datos \_ de soporte de TSMF en la estructura para contener información acerca de los formatos multimedia admitidos.
ms.assetid: 9aee9d6d-2182-44ec-ba8b-d2747d3edf71
ms.tgt_platform: multiple
keywords:
- Estructura de TSMF_SUPPORT_NODEDATA_IN Servicios de Escritorio remoto
- PTSMF_SUPPORT_NODEDATA_IN puntero de estructura Servicios de Escritorio remoto
topic_type:
- apiref
api_name:
- TSMF_SUPPORT_NODEDATA_IN
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4c36d18ea0e97da8df60475855c93755727fa87d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686012"
---
# <a name="tsmf_support_nodedata_in-structure"></a>TSMF \_ admite \_ NODEDATA \_ en la estructura

Se utiliza dentro de los [**\_ \_ datos \_ de soporte de TSMF en**](tsmf-support-data-in.md) la estructura para contener información acerca de los formatos multimedia admitidos.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct tagTSMF_SUPPORT_NODEDATA_IN {
  UINT32           byteCount;
  INT64            nodeId;
  UINT32           numMediaTypes;
  TS_AM_MEDIA_TYPE ...;
} TSMF_SUPPORT_NODEDATA_IN, *PTSMF_SUPPORT_NODEDATA_IN;
```



## <a name="members"></a>Miembros

<dl> <dt>

**byteCount**
</dt> <dd>

Tamaño de la estructura en bytes.

</dd> <dt>

**nodeId**
</dt> <dd>

El nodo.

</dd> <dt>

**numMediaTypes**
</dt> <dd>

Número de estructuras de formato multimedia.

</dd> <dt>

**...**
</dt> <dd>

Un número variable de estructuras que definen formatos multimedia de audio o vídeo. El **formatType** es **format \_ WaveFormatEx** para audio o **format \_ MFVideoFormat** para vídeo.

Para más información sobre esta estructura, consulte la [estructura de tipo de medio de TS \_ AM \_ \_ ](/openspecs/windows_protocols/ms-rdpev/22a57950-042e-48bd-8135-3580f3a3f934).

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>         |
| Servidor mínimo compatible<br/> | Windows Server 2008 R2<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**QueryProperty**](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-queryproperty)
</dt> <dt>

[**TSMF \_ admiten \_ datos \_ en**](tsmf-support-data-in.md)
</dt> </dl>

 

