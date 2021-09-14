---
title: TSMF_SUPPORT_NODEDATA_OUT estructura
description: Se usa dentro de la estructura \_ TSMF SUPPORT DATA OUT para contener información sobre los \_ \_ formatos multimedia admitidos.
ms.assetid: cac0af9e-6750-4735-b075-46c77aea7d41
ms.tgt_platform: multiple
keywords:
- TSMF_SUPPORT_NODEDATA_OUT estructura Servicios de Escritorio remoto
- PTSMF_SUPPORT_NODEDATA_OUT puntero de estructura Servicios de Escritorio remoto
topic_type:
- apiref
api_name:
- TSMF_SUPPORT_NODEDATA_OUT
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 517170e9d6580f69b59f71e0994351ebe0484ddc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127068591"
---
# <a name="tsmf_support_nodedata_out-structure"></a>TSMF \_ ADMITE LA estructura \_ NODEDATA \_ OUT

Se usa dentro de la [**estructura \_ TSMF SUPPORT DATA \_ \_ OUT**](tsmf-support-data-out.md) para contener información sobre los formatos multimedia admitidos.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct tagTSMF_SUPPORT_NODEDATA_OUT {
  INT64   nodeId;
  HRESULT hrSupportStatus;
  CLSID   clsidNewSink;
  UINT32  supportedMediaTypeIndex;
} TSMF_SUPPORT_NODEDATA_OUT, *PTSMF_SUPPORT_NODEDATA_OUT;
```



## <a name="members"></a>Members

<dl> <dt>

**nodeId**
</dt> <dd>

El nodo.

</dd> <dt>

**hrSupportStatus**
</dt> <dd>

Si se admite el receptor identificado *por el parámetro clsidNewSink.*

Los valores posibles son.

<dt>

0
</dt> <dd>

No compatible

</dd> <dt>

1
</dt> <dd>

Compatible

</dd> </dl>

Otros valores son indefinidos.

</dd> <dt>

**clsidNewSink**
</dt> <dd>

Receptor asociado al tipo de medio.

</dd> <dt>

**supportedMediaTypeIndex**
</dt> <dd>

Índice de base cero del tipo de medio admitido por el receptor.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>         |
| Servidor mínimo compatible<br/> | Windows Server 2008 R2<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**QueryProperty**](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-queryproperty)
</dt> <dt>

[**SALIDA DE DATOS \_ DE COMPATIBILIDAD \_ CON TSMF \_**](tsmf-support-data-out.md)
</dt> </dl>

 

 





