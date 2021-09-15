---
description: Devuelve información sobre un proceso que puede abrir recursos compartidos con acceso restringido.
ms.assetid: 669d9623-3a96-4661-9dae-3f283a990fe8
title: D3DAUTHENTICATEDQUERY_RESTRICTEDSHAREDRESOURCEPROCESS (D3d9types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDQUERY_RESTRICTEDSHAREDRESOURCEPROCESS
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 74bb829510fee4425648412f58d4f7cea74b1f72
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127569460"
---
# <a name="d3dauthenticatedquery_restrictedsharedresourceprocess"></a>D3DAUTHENTICATEDQUERY \_ RESTRICTEDSHAREDRESOURCEPROCESS

Devuelve información sobre un proceso que puede abrir recursos compartidos con acceso restringido.



| Requisito | Value |
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| GUID de consulta  | **D3DAUTHENTICATEDQUERY \_ RESTRICTEDSHAREDRESOURCEPROCESS**                                                                                           |
| Datos de entrada  | [**D3DAUTHENTICATEDCHANNEL \_ QUERYRESTRICTEDSHAREDRESOURCEPROCESS \_ INPUT**](d3dauthenticatedchannel-queryrestrictedsharedresourceprocess-input.md)   |
| Devolver datos | [**D3DAUTHENTICATEDCHANNEL \_ QUERYRESTRICTEDSHAREDRESOURCEPROCESS \_ OUTPUT**](d3dauthenticatedchannel-queryrestrictedsharedresourceprocess-output.md) |



 

## <a name="remarks"></a>Observaciones

Los siguientes tipos de canal admiten esta consulta:

-   **D3DAUTHENTICATEDCHANNEL \_ D3D9**
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

 

 




