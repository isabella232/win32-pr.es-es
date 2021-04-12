---
description: La interfaz ID3DXRenderToSurface se usa para generalizar el proceso de representación de las superficies.
ms.assetid: e9f2ca5e-faa3-45a8-94eb-16f354618e80
title: Interfaz ID3DXRenderToSurface (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToSurface
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 577e729e4e1a510dd24dc981b2b90bdca27dc0f9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362764"
---
# <a name="id3dxrendertosurface-interface"></a>Interfaz ID3DXRenderToSurface

La interfaz ID3DXRenderToSurface se usa para generalizar el proceso de representación de las superficies.

## <a name="members"></a>Miembros

La interfaz **ID3DXRenderToSurface** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DXRenderToSurface** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **ID3DXRenderToSurface** tiene estos métodos.



| Método                                                       | Descripción                                                                                                                                                                                     |
|:-------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**BeginScene**](id3dxrendertosurface--beginscene.md)       | Comienza una escena.<br/>                                                                                                                                                                      |
| [**EndScene**](id3dxrendertosurface--endscene.md)           | Finaliza una escena.<br/>                                                                                                                                                                        |
| [**GetDesc**](id3dxrendertosurface--getdesc.md)             | Recupera los parámetros de la superficie de representación.<br/>                                                                                                                                      |
| [**GetDevice**](id3dxrendertosurface--getdevice.md)         | Recupera el dispositivo Direct3D asociado a la superficie de representación.<br/>                                                                                                                    |
| [**OnLostDevice**](id3dxrendertosurface--onlostdevice.md)   | Utilice este método para liberar todas las referencias a los recursos de memoria de vídeo y eliminar todos los stateblocks. Se debe llamar a este método siempre que se pierda un dispositivo o antes de restablecer un dispositivo.<br/> |
| [**OnResetDevice**](id3dxrendertosurface--onresetdevice.md) | Use este método para volver a adquirir recursos y guardar el estado inicial.<br/>                                                                                                                      |



 

## <a name="remarks"></a>Observaciones

Las superficies se pueden usar de varias maneras, como objetivos de representación, representación fuera de pantalla o representación en texturas.

Una superficie se puede configurar mediante una ventanilla independiente mediante el método [**ID3DXRenderToSurface:: BeginScene**](id3dxrendertosurface--beginscene.md) para proporcionar una vista de representación personalizada. Si la superficie no es un destino de representación, se usa un destino de representación compatible y el resultado se copia en la superficie al final de la escena.

La interfaz **ID3DXRenderToSurface** se obtiene mediante una llamada a la función [**D3DXCreateRenderToSurface**](d3dxcreaterendertosurface.md) .

El tipo LPD3DXRENDERTOSURFACE se define como un puntero a la interfaz **ID3DXRenderToSurface** .


```
typedef interface ID3DXRenderToSurface ID3DXRenderToSurface;
typedef interface ID3DXRenderToSurface *LPD3DXRENDERTOSURFACE;
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Interfaces de D3DX](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
