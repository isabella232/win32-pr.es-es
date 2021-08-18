---
description: Códigos de estado que pueden devolver las funciones DXGI.
ms.assetid: dd7480b4-8218-4716-ab9f-74a9955b8aa7
title: DXGI_STATUS (DXGI.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2151c2c209feb630dfe445af2f5afc9d20048c08872fc73f9f5388abc5abb4b2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119951235"
---
# <a name="dxgi_status"></a>ESTADO DE \_ DXGI

Códigos de estado que pueden devolver las funciones DXGI.



| Constante o valor                                                                                                                                                                                                                                                                                      | Descripción                                                                                                                                                                                                                                                                                              |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DXGI_STATUS_OCCLUDED"></span><span id="dxgi_status_occluded"></span><dl> <dt>**DXGI \_ ESTADO \_ OCCLUDED**</dt> <dt>0x087A0001</dt> </dl>                                                 | El contenido de la ventana no está visible. Al recibir este estado, una aplicación puede detener la representación y usar DXGI \_ PRESENT TEST para determinar cuándo reanudar la \_ representación. No recibirá DXGI STATUS OCCLUDED si usa una cadena de intercambio de \_ \_ modelos de volteo.<br/>                                                                                                                           |
| <span id="DXGI_STATUS_MODE_CHANGED"></span><span id="dxgi_status_mode_changed"></span><dl> <dt>**DXGI \_ STATUS \_ MODE \_ CHANGED**</dt> <dt>0x087A0007</dt> </dl>                                    | Se ha cambiado el modo de presentación del escritorio, puede haber conversión de color o ajuste. La aplicación debe llamar a [**IDXGISwapChain::ResizeBuffers**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-resizebuffers) para que coincida con el nuevo modo de presentación.<br/>                                                                       |
| <span id="DXGI_STATUS_MODE_CHANGE_IN_PROGRESS"></span><span id="dxgi_status_mode_change_in_progress"></span><dl> <dt>**DXGI \_ CAMBIO \_ DE MODO DE ESTADO EN CURSO \_ \_ \_ 0X087A0008**</dt> <dt></dt> </dl> | [**IDXGISwapChain::ResizeTarget**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-resizetarget) e [**IDXGISwapChain::SetFullscreenState**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-setfullscreenstate) devolverán DXGI STATUS MODE CHANGE IN PROGRESS si se está produciendo una transición en modo de pantalla completa o ventana cuando se llama a cualquiera de las \_ \_ \_ \_ \_ API.<br/> |



## <a name="remarks"></a>Comentarios

El **valor HRESULT** de cada **valor DXGI \_ STATUS** se determina a partir de esta macro que se define en DXGItype.h:


```
#define _FACDXGI    0x87a
#define MAKE_DXGI_STATUS(code)  MAKE_HRESULT(0, _FACDXGI, code)
```



Por ejemplo, **DXGI \_ STATUS \_ OCCLUDED** se define como **0x087A0001**:


```
#define DXGI_STATUS_OCCLUDED                    MAKE_DXGI_STATUS(1)
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-----------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>DXGI.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Constantes DXGI](d3d10-graphics-reference-dxgi-constants.md)
</dt> </dl>

 

 




