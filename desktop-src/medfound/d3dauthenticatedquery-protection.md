---
description: Devuelve el nivel de protección actual del dispositivo.
ms.assetid: 335d21e8-2a98-4824-a60d-1969a40e8d24
title: D3DAUTHENTICATEDQUERY_PROTECTION (D3d9types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDQUERY_PROTECTION
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 85147d764d5b6580305723e9b05b127b116a660e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127172225"
---
# <a name="d3dauthenticatedquery_protection"></a>D3DAUTHENTICATEDQUERY \_ PROTECTION

Devuelve el nivel de protección actual del dispositivo.



| Requisito | Value |
|-------------|------------------------------------------------------------------------------------------------------------|
| GUID de consulta  | **D3DAUTHENTICATEDQUERY \_ PROTECTION**                                                                      |
| Datos de entrada  | [**ENTRADA DE CONSULTA D3DAUTHENTICATEDCHANNEL \_ \_**](d3dauthenticatedchannel-query-input.md)                       |
| Devolver datos | [**D3DAUTHENTICATEDCHANNEL \_ QUERYPROTECTION \_ OUTPUT**](d3dauthenticatedchannel-queryprotection-output.md) |



 

## <a name="remarks"></a>Observaciones

Esta consulta es válida para todos los tipos de canal.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 \[ aplicaciones de escritorio\]<br/>                                             |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/>                                |
| Encabezado<br/>                   | <dl> <dt>D3d9types.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Content Protection consultas](content-protection-queries.md)
</dt> <dt>

[Datos basados en GPU Content Protection](gpu-based-content-protection.md)
</dt> <dt>

[**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




