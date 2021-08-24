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
ms.openlocfilehash: df3eb4c515963e13d2a7919c58a6d55ca4b2a7600c429a33516093215b5ac0eb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119869015"
---
# <a name="tsmf_support_nodedata_out-structure"></a>TSMF \_ SUPPORT \_ NODEDATA OUT \_ structure

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



## <a name="members"></a>Miembros

<dl> <dt>

**nodeId**
</dt> <dd>

El nodo.

</dd> <dt>

**hrSupportStatus**
</dt> <dd>

Si se admite el receptor identificado por *el parámetro clsidNewSink.*

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

Otros valores no están definidos.

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



## <a name="see-also"></a>Vea también

<dl> <dt>

[**QueryProperty**](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-queryproperty)
</dt> <dt>

[**TSMF \_ ADMITE LA SALIDA DE \_ \_ DATOS**](tsmf-support-data-out.md)
</dt> </dl>

 

 





