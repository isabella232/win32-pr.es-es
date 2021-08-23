---
description: Devuelve identificadores a la sesión criptográfica y al dispositivo Direct3D que están asociados a un dispositivo descodificador de Aceleración de vídeo 2 (DXVA-2) de DirectX especificado.
ms.assetid: 90b3bcf3-2988-48de-8acd-62e385d4fdf0
title: D3DAUTHENTICATEDQUERY_CRYPTOSESSION (D3d9types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDQUERY_CRYPTOSESSION
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 3ee1cabc69122ebd7eb7d81c64eb761439e6a3c0cde20dd376c3581b9aed0738
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118974674"
---
# <a name="d3dauthenticatedquery_cryptosession"></a>D3DAUTHENTICATEDQUERY \_ CRYPTOSESSION

Devuelve identificadores a la sesión criptográfica y al dispositivo Direct3D que están asociados a un dispositivo descodificador de Aceleración de vídeo 2 (DXVA-2) de DirectX especificado.



| Requisito | Value |
|-------------|------------------------------------------------------------------------------------------------------------------|
| GUID de consulta  | **D3DAUTHENTICATEDQUERY \_ CRYPTOSESSION**                                                                         |
| Datos de entrada  | [**ENTRADA DE CONSULTA D3DAUTHENTICATEDCHANNEL \_ \_**](d3dauthenticatedchannel-query-input.md)                             |
| Devolver datos | [**D3DAUTHENTICATEDCHANNEL \_ QUERYCRYPTOSESSION \_ OUTPUT**](d3dauthenticatedchannel-querycryptosession-output.md) |



 

## <a name="remarks"></a>Comentarios

Los siguientes tipos de canal admiten esta consulta:

-   **HARDWARE DEL CONTROLADOR D3DAUTHENTICATEDCHANNEL \_ \_**
-   **SOFTWARE DEL CONTROLADOR D3DAUTHENTICATEDCHANNEL \_ \_**

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

 

 




