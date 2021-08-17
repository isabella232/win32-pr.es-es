---
description: Asocia una sesión criptográfica a un dispositivo descodificador directX Video Acceleration 2 (DXVA-2) y a un dispositivo Direct3D.
ms.assetid: d40fead7-8a86-426e-933e-13df21cdf50b
title: D3DAUTHENTICATEDCONFIGURE_CRYPTOSESSION (D3d9types.h)
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
ms.openlocfilehash: 3e1df4b58750d5b2d82eb518d5dfc0ef24bdbe4e5569ebcaf708b8df60691d04
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119449445"
---
# <a name="d3dauthenticatedconfigure_cryptosession"></a>D3DAUTHENTICATEDCONFIGURE \_ CRYPTOSESSION

Asocia una sesión criptográfica a un dispositivo descodificador directX Video Acceleration 2 (DXVA-2) y a un dispositivo Direct3D.



| Requisito | Value |
|--------------|-----------------------------------------------------------------------------------------------------------|
| GUID del comando | **D3DAUTHENTICATEDCONFIGURE \_ CRYPTOSESSION**                                                              |
| Datos de entrada   | [**D3DAUTHENTICATEDCHANNEL \_ CONFIGURECRYPTOSESSION**](d3dauthenticatedchannel-configurecryptosession.md) |



 

## <a name="remarks"></a>Comentarios

Después de enviar este comando, puede enviar la consulta [ \_ OUTPUTID D3DAUTHENTICATEDQUERY](d3dauthenticatedquery-outputid.md) para averiguar qué salidas de vídeo están asociadas a la sesión criptográfica.

Los siguientes tipos de canal admiten este comando:

-   **D3DAUTHENTICATEDCHANNEL \_ D3D9**
-   **SOFTWARE DEL CONTROLADOR D3DAUTHENTICATEDCHANNEL \_ \_**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                             |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/>                                |
| Header<br/>                   | <dl> <dt>D3d9types.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Content Protection comandos](content-protection-commands.md)
</dt> <dt>

[Datos basados en GPU Content Protection](gpu-based-content-protection.md)
</dt> <dt>

[**IDirect3DAuthenticatedChannel9::Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure)
</dt> </dl>

 

 




