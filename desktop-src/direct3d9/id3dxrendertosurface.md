---
description: La interfaz ID3DXRenderToSurface se usa para generalizar el proceso de representación en superficies.
ms.assetid: e9f2ca5e-faa3-45a8-94eb-16f354618e80
title: Interfaz ID3DXRenderToSurface (D3dx9core.h)
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
ms.openlocfilehash: 238e1870fd5bf1832ffbb3b5c3a5a49533ef122277a4000bafdbaa10112b4528
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117729511"
---
# <a name="id3dxrendertosurface-interface"></a>Interfaz ID3DXRenderToSurface

La interfaz ID3DXRenderToSurface se usa para generalizar el proceso de representación en superficies.

## <a name="members"></a>Miembros

La **interfaz ID3DXRenderToSurface** hereda de la [**interfaz IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **ID3DXRenderToSurface** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz ID3DXRenderToSurface** tiene estos métodos.



| Método                                                       | Descripción                                                                                                                                                                                     |
|:-------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**BeginScene**](id3dxrendertosurface--beginscene.md)       | Comienza una escena.<br/>                                                                                                                                                                      |
| [**EndScene**](id3dxrendertosurface--endscene.md)           | Finaliza una escena.<br/>                                                                                                                                                                        |
| [**GetDesc**](id3dxrendertosurface--getdesc.md)             | Recupera los parámetros de la superficie de representación.<br/>                                                                                                                                      |
| [**GetDevice**](id3dxrendertosurface--getdevice.md)         | Recupera el dispositivo Direct3D asociado a la superficie de representación.<br/>                                                                                                                    |
| [**OnLostDevice**](id3dxrendertosurface--onlostdevice.md)   | Use este método para liberar todas las referencias a los recursos de memoria de vídeo y eliminar todos los bloques de estado. Se debe llamar a este método cada vez que se pierde un dispositivo o antes de restablecer un dispositivo.<br/> |
| [**OnResetDevice**](id3dxrendertosurface--onresetdevice.md) | Use este método para volver a adquirir recursos y guardar el estado inicial.<br/>                                                                                                                      |



 

## <a name="remarks"></a>Comentarios

Las superficies se pueden usar de varias maneras, como destinos de representación, representación fuera de pantalla o representación en texturas.

Una superficie se puede configurar mediante una ventanilla independiente mediante el método [**ID3DXRenderToSurface::BeginScene,**](id3dxrendertosurface--beginscene.md) para proporcionar una vista de representación personalizada. Si la superficie no es un destino de representación, se usa un destino de representación compatible y el resultado se copia en la superficie al final de la escena.

La **interfaz ID3DXRenderToSurface** se obtiene llamando a la función [**D3DXCreateRenderToSurface.**](d3dxcreaterendertosurface.md)

El tipo LPD3DXRENDERTOSURFACE se define como un puntero a la **interfaz ID3DXRenderToSurface.**


```
typedef interface ID3DXRenderToSurface ID3DXRenderToSurface;
typedef interface ID3DXRenderToSurface *LPD3DXRENDERTOSURFACE;
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9core.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[D3DX Interfaces](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
