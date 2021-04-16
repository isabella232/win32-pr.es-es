---
description: Inicializa el canal autenticado.
ms.assetid: a74edbaa-af57-4f8e-9974-f6053f59377f
title: D3DAUTHENTICATEDCONFIGURE_INITIALIZE (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCONFIGURE_INITIALIZE
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 2cd3238b7a7eea27356ce76ec9c83bf8aea4d7f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696149"
---
# <a name="d3dauthenticatedconfigure_initialize"></a>D3DAUTHENTICATEDCONFIGURE \_ inicializar

Inicializa el canal autenticado.



| Requisito | Value |
|--------------|-----------------------------------------------------------------------------------------------------|
| GUID de comando | **D3DAUTHENTICATEDCONFIGURE \_ inicializar**                                                           |
| Datos de entrada   | [**D3DAUTHENTICATEDCHANNEL \_ CONFIGUREINITIALIZE**](d3dauthenticatedchannel-configureinitialize.md) |



 

## <a name="remarks"></a>Observaciones

Envíe este comando una vez, al principio de la sesión. Este comando solo se puede enviar una vez por cada canal autenticado. El número de secuencia de entrada se omite para este comando.

Los siguientes tipos de canal admiten este comando:

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

[Content Protection comandos](content-protection-commands.md)
</dt> <dt>

[Content Protection basados en GPU](gpu-based-content-protection.md)
</dt> <dt>

[**IDirect3DAuthenticatedChannel9:: configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure)
</dt> </dl>

 

 




