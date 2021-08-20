---
description: Devuelve el número de recursos compartidos protegidos que puede abrir cualquier proceso sin restricciones.
ms.assetid: afbd7bb9-de71-4992-919e-e1517228dc69
title: D3DAUTHENTICATEDQUERY_UNRESTRICTEDPROTECTEDSHAREDRESOURCECOUNT (D3d9types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDQUERY_UNRESTRICTEDPROTECTEDSHAREDRESOURCECOUNT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: a227d8aa23e7f070cebb1c73092bd0af170927eda582e417839375512e891df7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117879749"
---
# <a name="d3dauthenticatedquery_unrestrictedprotectedsharedresourcecount"></a>D3DAUTHENTICATEDQUERY \_ UNRESTRICTEDPROTECTEDSHAREDRESOURCECOUNT

Devuelve el número de recursos compartidos protegidos que puede abrir cualquier proceso sin restricciones.



| Requisito | Valor |
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| GUID de consulta  | **D3DAUTHENTICATEDQUERY \_ UNRESTRICTEDPROTECTEDSHAREDRESOURCECOUNT**                                                                                                    |
| Datos de entrada  | [**ENTRADA DE CONSULTA D3DAUTHENTICATEDCHANNEL \_ \_**](d3dauthenticatedchannel-query-input.md)                                                                                   |
| Devolver datos | [**D3DAUTHENTICATEDCHANNEL \_ QUERYUNRESTRICTEDPROTECTEDSHAREDRESOURCECOUNT \_ OUTPUT**](d3dauthenticatedchannel-queryunrestrictedprotectedsharedresourcecount-output.md) |



 

## <a name="remarks"></a>Comentarios

El único tipo de canal que admite esta consulta es **D3DAUTHENTICATEDCHANNEL \_ DRIVER \_ SOFTWARE**.

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

 

 




