---
description: Representa un acelerador de hardware para DirectX video Acceleration (DXVA) 1,0.
ms.assetid: 63f77cf9-4c04-4ddb-9582-cfcf86f66a2a
title: Interfaz IDirect3DDXVADevice9 (DXVA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DDXVADevice9
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: 192f47b8161893f9517bc976452eb8836da4bb53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715885"
---
# <a name="idirect3ddxvadevice9-interface"></a>Interfaz IDirect3DDXVADevice9

Representa un acelerador de hardware para DirectX video Acceleration (DXVA) 1,0.

## <a name="members"></a>Miembros

La interfaz **IDirect3DDXVADevice9** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IDirect3DDXVADevice9** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **IDirect3DDXVADevice9** tiene estos métodos.



| Método                                                  | Descripción                                                           |
|:--------------------------------------------------------|:----------------------------------------------------------------------|
| [**BeginFrame**](idirect3ddxvadevice9-beginframe.md)   | Comienza el procesamiento para crear una imagen descodificada.<br/>         |
| [**EndFrame**](idirect3ddxvadevice9-endframe.md)       | Finaliza el procesamiento para crear una imagen descodificada.<br/>           |
| [**Ejecut**](idirect3ddxvadevice9-execute.md)         | Realiza una operación de descodificación de DXVA. <br/>                       |
| [**QueryStatus**](idirect3ddxvadevice9-querystatus.md) | Consulta el estado de lectura y escritura de una superficie de descodificación de DXVA. <br/> |



 

## <a name="remarks"></a>Observaciones

Para obtener un puntero a esta interfaz, llame a [**IDirect3DVideoDevice9:: CreateDXVADevice**](idirect3dvideodevice9-createdxvadevice.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                    |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                              |
| Encabezado<br/>                   | <dl> <dt>DXVA. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Interfaces de vídeo de Direct3D](direct3d-video-interfaces.md)
</dt> </dl>

 

 
