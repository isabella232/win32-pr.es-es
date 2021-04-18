---
description: Códigos de estado que pueden ser devueltos por las funciones de DXGI.
ms.assetid: dd7480b4-8218-4716-ab9f-74a9955b8aa7
title: DXGI_STATUS (DXGI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b39c402880ccdcbda009402d56127e70a61543d0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707843"
---
# <a name="dxgi_status"></a>Estado de DXGI \_

Códigos de estado que pueden ser devueltos por las funciones de DXGI.



| Constante o valor                                                                                                                                                                                                                                                                                      | Descripción                                                                                                                                                                                                                                                                                              |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DXGI_STATUS_OCCLUDED"></span><span id="dxgi_status_occluded"></span><dl> <dt>**DXGI \_ ESTADO \_ ocluidos**</dt> <dt>0x087A0001</dt> </dl>                                                 | El contenido de la ventana no está visible. Al recibir este estado, una aplicación puede detener la representación y usar DXGI \_ present \_ test para determinar cuándo reanudar la representación. No recibirá \_ \_ el estado de DXGI ocluidos si usa una cadena de intercambio de Flip Model.<br/>                                                                                                                           |
| <span id="DXGI_STATUS_MODE_CHANGED"></span><span id="dxgi_status_mode_changed"></span><dl> <dt>**DXGI \_ Modo de estado \_ \_ cambiado**</dt> <dt>0x087A0007</dt> </dl>                                    | El modo de presentación del escritorio ha cambiado, puede que haya una conversión o ajuste de color. La aplicación debe llamar a [**IDXGISwapChain:: ResizeBuffers**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-resizebuffers) para que coincida con el nuevo modo de presentación.<br/>                                                                       |
| <span id="DXGI_STATUS_MODE_CHANGE_IN_PROGRESS"></span><span id="dxgi_status_mode_change_in_progress"></span><dl> <dt>**DXGI \_ \_ \_ Cambio en el modo de estado \_ en \_ curso**</dt> <dt>0x087A0008</dt> </dl> | [**IDXGISwapChain:: ResizeTarget**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-resizetarget) y [**IDXGISwapChain:: SetFullscreenState**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-setfullscreenstate) devolverán \_ \_ \_ \_ el cambio de modo de estado de DXGI en curso si se está \_ produciendo una transición de modo de pantalla completa o de ventana cuando se llama a una API.<br/> |



## <a name="remarks"></a>Observaciones

El valor **HRESULT** para cada valor de **\_ Estado de DXGI** se determina a partir de esta macro que se define en DXGItype. h:


```
#define _FACDXGI    0x87a
#define MAKE_DXGI_STATUS(code)  MAKE_HRESULT(0, _FACDXGI, code)
```



Por ejemplo, **el \_ estado \_ de DXGI ocluidos** se define como **0x087A0001**:


```
#define DXGI_STATUS_OCCLUDED                    MAKE_DXGI_STATUS(1)
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-----------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>DXGI. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Constantes de DXGI](d3d10-graphics-reference-dxgi-constants.md)
</dt> </dl>

 

 




