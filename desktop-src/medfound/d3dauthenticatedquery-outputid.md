---
description: Devuelve uno de los identificadores de salida asociados a una sesión criptográfica y un dispositivo Direct3D especificados.
ms.assetid: 7b56055a-fb36-4e54-9bee-ab9401b09267
title: D3DAUTHENTICATEDQUERY_OUTPUTID (D3d9types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDQUERY_OUTPUTID
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 7e8d735cf23ed5bac26ca26b779ba440f7a48301bf33f7de34d1986e75241324
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119942755"
---
# <a name="d3dauthenticatedquery_outputid"></a>D3DAUTHENTICATEDQUERY \_ OUTPUTID

Devuelve uno de los identificadores de salida asociados a una sesión criptográfica y un dispositivo Direct3D especificados.



| Requisito | Value |
|-------------|--------------------------------------------------------------------------------------------------------|
| GUID de consulta  | **D3DAUTHENTICATEDQUERY \_ OUTPUTID**                                                                    |
| Datos de entrada  | [**D3DAUTHENTICATEDCHANNEL \_ QUERYOUTPUTID \_ INPUT**](d3dauthenticatedchannel-queryoutputid-input.md)   |
| Devolver datos | [**D3DAUTHENTICATEDCHANNEL \_ QUERYOUTPUTID \_ OUTPUT**](d3dauthenticatedchannel-queryoutputid-output.md) |



 

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

 

 




