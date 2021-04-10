---
description: Devuelve los identificadores de la sesión criptográfica y el dispositivo Direct3D que están asociados a un dispositivo descodificador DirectX video Acceleration 2 (DXVA-2) especificado.
ms.assetid: 90b3bcf3-2988-48de-8acd-62e385d4fdf0
title: D3DAUTHENTICATEDQUERY_CRYPTOSESSION (D3d9types. h)
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
ms.openlocfilehash: e824514c3fef4e3e036b8f2973d3a958c4e135ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275126"
---
# <a name="d3dauthenticatedquery_cryptosession"></a>D3DAUTHENTICATEDQUERY \_ CRYPTOSESSION

Devuelve los identificadores de la sesión criptográfica y el dispositivo Direct3D que están asociados a un dispositivo descodificador DirectX video Acceleration 2 (DXVA-2) especificado.



| Requisito | Value |
|-------------|------------------------------------------------------------------------------------------------------------------|
| GUID de consulta  | **D3DAUTHENTICATEDQUERY \_ CRYPTOSESSION**                                                                         |
| Datos de entrada  | [**\_Entrada de consulta de D3DAUTHENTICATEDCHANNEL \_**](d3dauthenticatedchannel-query-input.md)                             |
| Devolver datos | [**Salida de D3DAUTHENTICATEDCHANNEL \_ QUERYCRYPTOSESSION \_**](d3dauthenticatedchannel-querycryptosession-output.md) |



 

## <a name="remarks"></a>Observaciones

Los siguientes tipos de canal admiten esta consulta:

-   **\_Hardware del controlador D3DAUTHENTICATEDCHANNEL \_**
-   **\_Software de controlador D3DAUTHENTICATEDCHANNEL \_**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                             |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]<br/>                                |
| Encabezado<br/>                   | <dl> <dt>D3d9types. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Consultas Content Protection](content-protection-queries.md)
</dt> <dt>

[Content Protection basados en GPU](gpu-based-content-protection.md)
</dt> <dt>

[**IDirect3DAuthenticatedChannel9:: Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




