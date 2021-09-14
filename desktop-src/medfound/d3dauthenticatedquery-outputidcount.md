---
description: Devuelve el número de identificadores de salida asociados a una sesión criptográfica y un dispositivo Direct3D especificados.
ms.assetid: a5b17250-6a40-40a9-93b6-3b98b56b09d6
title: D3DAUTHENTICATEDQUERY_OUTPUTIDCOUNT (D3d9types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDQUERY_OUTPUTIDCOUNT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 624b9ca0ee96f71fb9d3cb655aa9c10030a40efe
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127172226"
---
# <a name="d3dauthenticatedquery_outputidcount"></a>D3DAUTHENTICATEDQUERY \_ OUTPUTIDCOUNT

Devuelve el número de identificadores de salida asociados a una sesión criptográfica y un dispositivo Direct3D especificados.



| Requisito | Value |
|-------------|------------------------------------------------------------------------------------------------------------------|
| GUID de consulta  | **D3DAUTHENTICATEDQUERY \_ OUTPUTIDCOUNT**                                                                         |
| Datos de entrada  | [**D3DAUTHENTICATEDCHANNEL \_ QUERYOUTPUTIDCOUNT \_ INPUT**](d3dauthenticatedchannel-queryoutputidcount-input.md)   |
| Devolver datos | [**D3DAUTHENTICATEDCHANNEL \_ QUERYOUTPUTIDCOUNT \_ OUTPUT**](d3dauthenticatedchannel-queryoutputidcount-output.md) |



 

## <a name="remarks"></a>Observaciones

Los siguientes tipos de canal admiten esta consulta:

-   **HARDWARE DEL CONTROLADOR D3DAUTHENTICATEDCHANNEL \_ \_**
-   **SOFTWARE DEL CONTROLADOR D3DAUTHENTICATEDCHANNEL \_ \_**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                             |
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

 

 




