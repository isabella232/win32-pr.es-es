---
title: Estructura de TSMF_SUPPORT_DATA_IN
description: Contiene información acerca de los formatos de medios. | Estructura de TSMF_SUPPORT_DATA_IN
ms.assetid: cd1a8295-22b7-4d75-8325-94da4d7380d0
ms.tgt_platform: multiple
keywords:
- Estructura de TSMF_SUPPORT_DATA_IN Servicios de Escritorio remoto
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
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105689776"
---
# <a name="tsmf_support_data_in-structure"></a>TSMF \_ admiten \_ datos \_ en la estructura

Contiene información acerca de los formatos de medios. El método [**QueryProperty**](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-queryproperty) usa esta estructura durante las consultas **\_ \_ \_ \_ compatibles con el formato MF de la consulta Wrds** .

## <a name="syntax"></a>Sintaxis


```C++
typedef struct tagTSMF_SUPPORT_DATA_IN {
  GUID                     guidMfSession;
  UINT32                   numEntries;
  TSMF_SUPPORT_NODEDATA_IN ...;
} TSMF_SUPPORT_DATA_IN, *PTSMF_SUPPORT_DATA_IN;
```



## <a name="members"></a>Miembros

<dl> <dt>

**guidMfSession**
</dt> <dd>

La sesión.

</dd> <dt>

**numEntries**
</dt> <dd>

El número de estructuras en los datos de longitud variable.

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

[**TSMF \_ admite \_ NODEDATA \_ en**](tsmf-support-nodedata-in.md)
</dt> </dl>

 

 





