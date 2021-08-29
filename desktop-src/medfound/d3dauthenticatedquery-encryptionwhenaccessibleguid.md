---
description: Devuelve uno de los tipos de cifrado que se pueden usar para cifrar el contenido antes de que sea accesible para la CPU o el bus.
ms.assetid: 263c6f00-8bc9-4e9c-8b98-fb8f87c6c008
title: D3DAUTHENTICATEDQUERY_ENCRYPTIONWHENACCESSIBLEGUID (D3d9types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDQUERY_ENCRYPTIONWHENACCESSIBLEGUID
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: cda11acf707851f23728d7958716df5ce319c6ac4c49d63c98e0aa90cd961245
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119828645"
---
# <a name="d3dauthenticatedquery_encryptionwhenaccessibleguid"></a>CIFRADO D3DAUTHENTICATEDQUERYWHENACCESSIBLEGUID \_

Devuelve uno de los tipos de cifrado que se pueden usar para cifrar el contenido antes de que sea accesible para la CPU o el bus.



| Requisito | Value |
|-------------|------------------------------------------------------------------------------------------------------------------------------------|
| GUID de consulta  | **CIFRADO D3DAUTHENTICATEDQUERYWHENACCESSIBLEGUID \_**                                                                            |
| Datos de entrada  | [**D3DAUTHENTICATEDCHANNEL \_ QUERYEVICTIONENCRYPTIONGUID \_ INPUT**](d3dauthenticatedchannel-queryevictionencryptionguid-input.md)   |
| Devolver datos | [**D3DAUTHENTICATEDCHANNEL \_ QUERYEVICTIONENCRYPTIONGUID \_ OUTPUT**](d3dauthenticatedchannel-queryevictionencryptionguid-output.md) |



 

## <a name="remarks"></a>Comentarios

Los siguientes tipos de canal admiten esta consulta:

-   **HARDWARE DEL CONTROLADOR D3DAUTHENTICATEDCHANNEL \_ \_**
-   **SOFTWARE DE CONTROLADOR D3DAUTHENTICATEDCHANNEL \_ \_**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                             |
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

 

 




