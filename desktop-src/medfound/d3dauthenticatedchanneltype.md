---
description: Especifica el tipo de canal de Direct3D autenticado.
ms.assetid: 99a7664e-b0c8-4e66-ad3b-c6ad039ef6eb
title: Enumeración D3DAUTHENTICATEDCHANNELTYPE (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNELTYPE
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 5c0cab8a0a208bfb1a005166740dcc64c319c6e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659782"
---
# <a name="d3dauthenticatedchanneltype-enumeration"></a>Enumeración D3DAUTHENTICATEDCHANNELTYPE

Especifica el tipo de canal de Direct3D autenticado.

## <a name="syntax"></a>Sintaxis


```C++
typedef enum  { 
  D3DAUTHENTICATEDCHANNEL_D3D9             = 1,
  D3DAUTHENTICATEDCHANNEL_DRIVER_SOFTWARE  = 2,
  D3DAUTHENTICATEDCHANNEL_DRIVER_HARDWARE  = 3
} D3DAUTHENTICATEDCHANNELTYPE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DAUTHENTICATEDCHANNEL_D3D9"></span><span id="d3dauthenticatedchannel_d3d9"></span>**D3DAUTHENTICATEDCHANNEL \_ D3D9**
</dt> <dd>

Canal de Direct3D 9. Este canal proporciona comunicación con el tiempo de ejecución de Direct3D.

</dd> <dt>

<span id="D3DAUTHENTICATEDCHANNEL_DRIVER_SOFTWARE"></span><span id="d3dauthenticatedchannel_driver_software"></span>**\_Software de controlador D3DAUTHENTICATEDCHANNEL \_**
</dt> <dd>

Canal del controlador de software. Este canal proporciona comunicación con un controlador que implementa mecanismos de protección de contenido en el software.

</dd> <dt>

<span id="D3DAUTHENTICATEDCHANNEL_DRIVER_HARDWARE"></span><span id="d3dauthenticatedchannel_driver_hardware"></span>**\_Hardware del controlador D3DAUTHENTICATEDCHANNEL \_**
</dt> <dd>

Canal del controlador de hardware. Este canal proporciona comunicación con un controlador que implementa mecanismos de protección de contenido en el hardware de la GPU.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                                              |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]<br/>                                                 |
| Encabezado<br/>                   | <dl> <dt>D3d9types. h (incluye d3d9. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Enumeraciones de vídeo de Direct3D](direct3d-video-enumerations.md)
</dt> <dt>

[**IDirect3DDevice9Video::CreateAuthenticatedChannel**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9video-createauthenticatedchannel)
</dt> </dl>

 

 




