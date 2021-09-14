---
title: TSMF_SUPPORT_DATA_IN estructura
description: Contiene información sobre los formatos multimedia. | TSMF_SUPPORT_DATA_IN estructura
ms.assetid: cd1a8295-22b7-4d75-8325-94da4d7380d0
ms.tgt_platform: multiple
keywords:
- TSMF_SUPPORT_DATA_IN estructura Servicios de Escritorio remoto
- PTSMF_SUPPORT_DATA_IN puntero de estructura Servicios de Escritorio remoto
topic_type:
- apiref
api_name:
- TSMF_SUPPORT_DATA_IN
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2072363978cb0e70d64a09d855ed2861341e9cf0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127374398"
---
# <a name="tsmf_support_data_in-structure"></a>Estructura TSMF \_ SUPPORT \_ DATA \_ IN

Contiene información sobre los formatos multimedia. El método [**QueryProperty**](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-queryproperty) usa esta estructura durante las consultas **\_ WRDS QUERY MF FORMAT \_ \_ \_ SUPPORT.**

## <a name="syntax"></a>Sintaxis


```C++
typedef struct tagTSMF_SUPPORT_DATA_IN {
  GUID                     guidMfSession;
  UINT32                   numEntries;
  TSMF_SUPPORT_NODEDATA_IN ...;
} TSMF_SUPPORT_DATA_IN, *PTSMF_SUPPORT_DATA_IN;
```



## <a name="members"></a>Members

<dl> <dt>

**guidMfSession**
</dt> <dd>

La sesión.

</dd> <dt>

**numEntries**
</dt> <dd>

Número de estructuras en los datos de longitud variable.

</dd> <dt>

**...**
</dt> <dd>

Número variable de estructuras que contienen datos de formato multimedia.

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

[**COMPATIBILIDAD DE TSMF \_ \_ CON NODEDATA \_ EN**](tsmf-support-nodedata-in.md)
</dt> </dl>

 

 





