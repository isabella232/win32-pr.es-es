---
description: Devuelve el número de procesos que pueden abrir recursos compartidos con acceso restringido.
ms.assetid: e1b9ef18-fd08-4639-9ba9-4bccd33f5d16
title: D3DAUTHENTICATEDQUERY_RESTRICTEDSHAREDRESOURCEPROCESSCOUNT (D3d9types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDQUERY_RESTRICTEDSHAREDRESOURCEPROCESSCOUNT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 5238d027b5fe8ed7ebd1ab941b3877d5b545239b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127569457"
---
# <a name="d3dauthenticatedquery_restrictedsharedresourceprocesscount"></a>D3DAUTHENTICATEDQUERY \_ RESTRICTEDSHAREDRESOURCEPROCESSCOUNT

Devuelve el número de procesos que pueden abrir recursos compartidos con acceso restringido.



| Requisito | Value |
|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| GUID de consulta  | **D3DAUTHENTICATEDQUERY \_ RESTRICTEDSHAREDRESOURCEPROCESSCOUNT**                                                                                                |
| Datos de entrada  | [**ENTRADA DE CONSULTA D3DAUTHENTICATEDCHANNEL \_ \_**](d3dauthenticatedchannel-query-input.md)                                                                           |
| Devolver datos | [**D3DAUTHENTICATEDCHANNEL \_ QUERYRESTRICTEDSHAREDRESOURCEPROCESSCOUNT \_ OUTPUT**](d3dauthenticatedchannel-queryrestrictedsharedresourceprocesscount-output.md) |



 

## <a name="remarks"></a>Observaciones

Los siguientes tipos de canal admiten esta consulta:

-   **D3DAUTHENTICATEDCHANNEL \_ D3D9**
-   **SOFTWARE DE CONTROLADOR D3DAUTHENTICATEDCHANNEL \_ \_**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio solo\]<br/>                                             |
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

 

 




