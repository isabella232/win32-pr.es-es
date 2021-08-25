---
title: TSMF_SUPPORT_DATA_OUT estructura
description: Contiene información sobre los formatos multimedia. | TSMF_SUPPORT_DATA_OUT estructura
ms.assetid: 987ede31-ad15-489f-90e5-fb707c6b38a9
ms.tgt_platform: multiple
keywords:
- TSMF_SUPPORT_DATA_OUT estructura Servicios de Escritorio remoto
- PTSMF_SUPPORT_DATA_OUT puntero de estructura Servicios de Escritorio remoto
topic_type:
- apiref
api_name:
- TSMF_SUPPORT_DATA_OUT
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8577266c2e259e7a7e4bb70310837eee1d743905e0e0d166e5797bc51a1f1b45
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119869025"
---
# <a name="tsmf_support_data_out-structure"></a>Estructura TSMF \_ SUPPORT \_ DATA \_ OUT

Contiene información sobre los formatos multimedia. El método [**QueryProperty**](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-queryproperty) usa esta estructura durante las consultas **\_ WRDS QUERY MF FORMAT \_ \_ \_ SUPPORT.**

## <a name="syntax"></a>Sintaxis


```C++
typedef struct tagTSMF_SUPPORT_DATA_OUT {
  GUID                      guidMfSession;
  UINT32                    numEntries;
  TSMF_SUPPORT_NODEDATA_OUT ...;
} TSMF_SUPPORT_DATA_OUT, *PTSMF_SUPPORT_DATA_OUT;
```



## <a name="members"></a>Miembros

<dl> <dt>

**guidMfSession**
</dt> <dd>

Debe coincidir con la **propiedad guidMfSession** de la estructura [**\_ TSMF SUPPORT DATA \_ \_ IN**](tsmf-support-data-in.md) correspondiente.

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

[**TSMF \_ ADMITE \_ NODEDATA \_ OUT**](tsmf-support-nodedata-out.md)
</dt> </dl>

 

 





