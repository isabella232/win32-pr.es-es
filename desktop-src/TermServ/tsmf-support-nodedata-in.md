---
title: TSMF_SUPPORT_NODEDATA_IN estructura
description: Se usa dentro de la estructura SUPPORT DATA IN de TSMF \_ para contener información sobre los \_ \_ formatos multimedia admitidos.
ms.assetid: 9aee9d6d-2182-44ec-ba8b-d2747d3edf71
ms.tgt_platform: multiple
keywords:
- TSMF_SUPPORT_NODEDATA_IN estructura Servicios de Escritorio remoto
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
ms.openlocfilehash: 5e1920ca627a7da8aef2d49a6930b03f0906cfd912e2a2a584b20d8e8382b706
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117755727"
---
# <a name="tsmf_support_nodedata_in-structure"></a>TSMF \_ SUPPORT \_ NODEDATA IN \_ structure

Se usa dentro de la [**estructura SUPPORT DATA \_ \_ \_ IN de TSMF**](tsmf-support-data-in.md) para contener información sobre los formatos multimedia admitidos.

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

Número variable de estructuras que definen formatos multimedia de audio o vídeo. FormatType **es** **FORMAT \_ WaveFormatEx** para audio o **FORMAT \_ MFVideoFormat** para vídeo.

Para obtener más información sobre esta estructura, vea [TS \_ AM MEDIA \_ TYPE \_ Structure](/openspecs/windows_protocols/ms-rdpev/22a57950-042e-48bd-8135-3580f3a3f934).

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

[**DATOS DE COMPATIBILIDAD DE TSMF \_ \_ \_ EN**](tsmf-support-data-in.md)
</dt> </dl>

 

