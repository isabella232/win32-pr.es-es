---
description: Devuelve el tipo de cifrado que se aplica antes de que el contenido sea accesible para la CPU o el bus.
ms.assetid: 89526bb2-1316-4730-b599-3690b1838c3e
title: D3DAUTHENTICATEDQUERY_CURRENTENCRYPTIONWHENACCESSIBLE (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDQUERY_CURRENTENCRYPTIONWHENACCESSIBLE
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: a8b3374e6d50a50d32b60113318e5d1099083226
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275127"
---
# <a name="d3dauthenticatedquery_currentencryptionwhenaccessible"></a>D3DAUTHENTICATEDQUERY \_ CURRENTENCRYPTIONWHENACCESSIBLE

Devuelve el tipo de cifrado que se aplica antes de que el contenido sea accesible para la CPU o el bus.



| Requisito | Value |
|-------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| GUID de consulta  | **D3DAUTHENTICATEDQUERY \_ CURRENTENCRYPTIONWHENACCESSIBLE**                                                                                   |
| Datos de entrada  | [**\_Entrada de consulta de D3DAUTHENTICATEDCHANNEL \_**](d3dauthenticatedchannel-query-input.md)                                                         |
| Devolver datos | [**Salida de D3DAUTHENTICATEDCHANNEL \_ QUERYUNCOMPRESSEDENCRYPTIONLEVEL \_**](d3dauthenticatedchannel-queryuncompressedencryptionlevel-output.md) |



 

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

 

 




