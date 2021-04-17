---
description: Asocia una sesión criptográfica a un dispositivo descodificador DirectX video Acceleration 2 (DXVA-2) y un dispositivo Direct3D.
ms.assetid: d40fead7-8a86-426e-933e-13df21cdf50b
title: D3DAUTHENTICATEDCONFIGURE_CRYPTOSESSION (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCONFIGURE_CRYPTOSESSION
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 4b6fda19aef9629214aaa410fd43c4d64f16dd29
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659781"
---
# <a name="d3dauthenticatedconfigure_cryptosession"></a>D3DAUTHENTICATEDCONFIGURE \_ CRYPTOSESSION

Asocia una sesión criptográfica a un dispositivo descodificador DirectX video Acceleration 2 (DXVA-2) y un dispositivo Direct3D.



| Requisito | Value |
|--------------|-----------------------------------------------------------------------------------------------------------|
| GUID de comando | **D3DAUTHENTICATEDCONFIGURE \_ CRYPTOSESSION**                                                              |
| Datos de entrada   | [**D3DAUTHENTICATEDCHANNEL \_ CONFIGURECRYPTOSESSION**](d3dauthenticatedchannel-configurecryptosession.md) |



 

## <a name="remarks"></a>Observaciones

Después de enviar este comando, puede enviar la consulta [D3DAUTHENTICATEDQUERY \_ OUTPUTID](d3dauthenticatedquery-outputid.md) para averiguar qué salidas de vídeo están asociadas a la sesión criptográfica.

Los siguientes tipos de canal admiten este comando:

-   **D3DAUTHENTICATEDCHANNEL \_ D3D9**
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

 

 




