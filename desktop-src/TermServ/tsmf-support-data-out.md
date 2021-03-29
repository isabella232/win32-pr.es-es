---
title: Estructura de TSMF_SUPPORT_DATA_OUT
description: Contiene información acerca de los formatos de medios. | Estructura de TSMF_SUPPORT_DATA_OUT
ms.assetid: 987ede31-ad15-489f-90e5-fb707c6b38a9
ms.tgt_platform: multiple
keywords:
- Estructura de TSMF_SUPPORT_DATA_OUT Servicios de Escritorio remoto
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
ms.openlocfilehash: 9705c4c2c27eaff904e09364b029bd74ebd05d6c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104003536"
---
# <a name="tsmf_support_data_out-structure"></a>\_Estructura de \_ salida de datos de TSMF support \_

Contiene información acerca de los formatos de medios. El método [**QueryProperty**](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-queryproperty) usa esta estructura durante las consultas **\_ \_ \_ \_ compatibles con el formato MF de la consulta Wrds** .

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

Debe coincidir con la propiedad **guidMfSession** en los [**\_ \_ datos de soporte \_ de TSMF correspondientes en**](tsmf-support-data-in.md) la estructura.

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

[**\_compatibilidad con TSMF \_ NODEDATA \_ out**](tsmf-support-nodedata-out.md)
</dt> </dl>

 

 





