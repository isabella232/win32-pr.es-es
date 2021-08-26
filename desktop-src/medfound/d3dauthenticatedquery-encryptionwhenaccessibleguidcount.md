---
description: Devuelve el número de tipos de cifrado que se pueden usar para cifrar el contenido antes de que sea accesible para la CPU o el bus.
ms.assetid: 442b80f5-8467-427d-a01e-5d22f6ddafea
title: D3DAUTHENTICATEDQUERY_ENCRYPTIONWHENACCESSIBLEGUIDCOUNT (D3d9types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDQUERY_ENCRYPTIONWHENACCESSIBLEGUIDCOUNT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: f47074947cc2f758d35691e05dda9b39f2f823feb6d647a7d77c0a3cc0030c75
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119942765"
---
# <a name="d3dauthenticatedquery_encryptionwhenaccessibleguidcount"></a>CIFRADO D3DAUTHENTICATEDQUERYWHENACCESSIBLEGUIDCOUNT \_

Devuelve el número de tipos de cifrado que se pueden usar para cifrar el contenido antes de que sea accesible para la CPU o el bus.



| Requisito | Value |
|-------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| GUID de consulta  | **CIFRADO D3DAUTHENTICATEDQUERYWHENACCESSIBLEGUIDCOUNT \_**                                                                                 |
| Datos de entrada  | [**ENTRADA DE CONSULTA D3DAUTHENTICATEDCHANNEL \_ \_**](d3dauthenticatedchannel-query-input.md)                                                         |
| Devolver datos | [**D3DAUTHENTICATEDCHANNEL \_ QUERYEVICTIONENCRYPTIONGUIDCOUNT \_ OUTPUT**](d3dauthenticatedchannel-queryevictionencryptionguidcount-output.md) |



 

## <a name="remarks"></a>Comentarios

Los siguientes tipos de canal admiten esta consulta:

-   **HARDWARE DEL CONTROLADOR D3DAUTHENTICATEDCHANNEL \_ \_**
-   **SOFTWARE DE CONTROLADOR D3DAUTHENTICATEDCHANNEL \_ \_**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows solo 7 \[ aplicaciones de escritorio\]<br/>                                             |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/>                                |
| Header<br/>                   | <dl> <dt>D3d9types.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Content Protection consultas](content-protection-queries.md)
</dt> <dt>

[Datos basados en GPU Content Protection](gpu-based-content-protection.md)
</dt> <dt>

[**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




