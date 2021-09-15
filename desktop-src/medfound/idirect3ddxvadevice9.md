---
description: Representa un acelerador de hardware para DirectX Video Acceleration (DXVA) 1.0.
ms.assetid: 63f77cf9-4c04-4ddb-9582-cfcf86f66a2a
title: Interfaz IDirect3DDXVADevice9 (Dxva.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127581061"
---
# <a name="idirect3ddxvadevice9-interface"></a>Interfaz IDirect3DDXVADevice9

Representa un acelerador de hardware para DirectX Video Acceleration (DXVA) 1.0.

## <a name="members"></a>Members

La **interfaz IDirect3DDXVADevice9** hereda de la [**interfaz IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IDirect3DDXVADevice9** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IDirect3DDXVADevice9** tiene estos métodos.



| Método                                                  | Descripción                                                           |
|:--------------------------------------------------------|:----------------------------------------------------------------------|
| [**BeginFrame**](idirect3ddxvadevice9-beginframe.md)   | Comienza el procesamiento para crear una imagen descodificada.<br/>         |
| [**EndFrame**](idirect3ddxvadevice9-endframe.md)       | Finaliza el procesamiento para crear una imagen descodificada.<br/>           |
| [**Execute**](idirect3ddxvadevice9-execute.md)         | Realiza una operación de decodificación dxva. <br/>                       |
| [**QueryStatus**](idirect3ddxvadevice9-querystatus.md) | Consulta el estado de lectura y escritura de una superficie de decoding DXVA. <br/> |



 

## <a name="remarks"></a>Observaciones

Para obtener un puntero a esta interfaz, llame a [**IDirect3DVideoDevice9::CreateDXVADevice**](idirect3dvideodevice9-createdxvadevice.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                    |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                              |
| Encabezado<br/>                   | <dl> <dt>Dxva.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Interfaces de vídeo de Direct3D](direct3d-video-interfaces.md)
</dt> </dl>

 

 
