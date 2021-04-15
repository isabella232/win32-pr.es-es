---
description: Marcas para las opciones de creación de recursos y superficie.
ms.assetid: b5026566-89b5-458e-b36d-a55e5f8c10c1
title: DXGI_USAGE (DXGI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e55e99d86201c76fbe2ec229b13b5831d767ff34
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707841"
---
# <a name="dxgi_usage"></a>uso de DXGI \_

Marcas para las opciones de creación de recursos y superficie.



| Constante o valor                                                                                                                                                                                                                                                                                  | Descripción                                                                                                                                                                                                                                                                                                                     |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DXGI_USAGE_BACK_BUFFER"></span><span id="dxgi_usage_back_buffer"></span><dl> <dt>**DXGI \_ <<  \_ de \_ búfer de reserva de uso**</dt> <dt>1L (2 + 4)</dt> </dl>                             | La superficie o el recurso se utiliza como búfer de reserva. No es necesario pasar el **\_ búfer de \_ retroceso \_ de uso de DXGI** al crear una cadena de intercambio. Sin embargo, puede determinar si un recurso pertenece a una cadena de intercambio cuando llama a [**IDXGIResource:: GetUsage**](/windows/desktop/api/DXGI/nf-dxgi-idxgiresource-getusage) y obtiene el **búfer de retroceso de uso de DXGI \_ \_ \_**.<br/> |
| <span id="DXGI_USAGE_DISCARD_ON_PRESENT"></span><span id="dxgi_usage_discard_on_present"></span><dl> <dt>**DXGI \_ USO \_ descartado \_ en \_**</dt> la <dt>1L actual <<  (5 + 4)</dt> </dl>       | Esta marca solo es para uso interno.<br/>                                                                                                                                                                                                                                                                                  |
| <span id="DXGI_USAGE_READ_ONLY"></span><span id="dxgi_usage_read_only"></span><dl> <dt>**DXGI \_ USO \_ de \_ solo lectura**</dt> <dt>1L <<  (4 + 4)</dt> </dl>                                   | Use la superficie o el recurso solo para lectura.<br/>                                                                                                                                                                                                                                                                        |
| <span id="DXGI_USAGE_RENDER_TARGET_OUTPUT"></span><span id="dxgi_usage_render_target_output"></span><dl> <dt>**DXGI \_ 1L \_ de \_ \_ salida de destino de representación de uso**</dt> <dt> <<  (1 + 4)</dt> </dl> | Use la superficie o el recurso como destino de representación de salida.<br/>                                                                                                                                                                                                                                                              |
| <span id="DXGI_USAGE_SHADER_INPUT"></span><span id="dxgi_usage_shader_input"></span><dl> <dt>**DXGI \_ <<  de \_ \_ entrada del sombreador de uso**</dt> <dt>1L (0 + 4)</dt> </dl>                          | Use la superficie o el recurso como entrada para un sombreador.<br/>                                                                                                                                                                                                                                                                 |
| <span id="DXGI_USAGE_SHARED"></span><span id="dxgi_usage_shared"></span><dl> <dt>**DXGI \_ USO \_ compartido**</dt> de <dt>1L <<  (3 + 4)</dt> </dl>                                             | Comparta la superficie o el recurso.<br/>                                                                                                                                                                                                                                                                                       |
| <span id="DXGI_USAGE_UNORDERED_ACCESS"></span><span id="dxgi_usage_unordered_access"></span><dl> <dt>**DXGI \_ \_ \_ Acceso desordenado de uso**</dt> <dt>1L <<  (6 + 4)</dt> </dl>              | Use la superficie o el recurso para el acceso desordenado.<br/>                                                                                                                                                                                                                                                                    |



## <a name="remarks"></a>Observaciones

Cada marca se define como un entero sin signo.

``` syntax
#define DXGI_CPU_ACCESS_NONE    ( 0 )
#define DXGI_CPU_ACCESS_DYNAMIC    ( 1 )
#define DXGI_CPU_ACCESS_READ_WRITE    ( 2 )
#define DXGI_CPU_ACCESS_SCRATCH    ( 3 )
#define DXGI_CPU_ACCESS_FIELD        15
#define DXGI_USAGE_SHADER_INPUT             ( 1L << (0 + 4) )
#define DXGI_USAGE_RENDER_TARGET_OUTPUT     ( 1L << (1 + 4) )
#define DXGI_USAGE_BACK_BUFFER              ( 1L << (2 + 4) )
#define DXGI_USAGE_SHARED                   ( 1L << (3 + 4) )
#define DXGI_USAGE_READ_ONLY                ( 1L << (4 + 4) )
#define DXGI_USAGE_DISCARD_ON_PRESENT       ( 1L << (5 + 4) )
#define DXGI_USAGE_UNORDERED_ACCESS         ( 1L << (6 + 4) )
typedef UINT DXGI_USAGE;
```

Estas opciones de marca se usan en una llamada al método [**IDXGIFactory:: CreateSwapChain**](/windows/desktop/api/DXGI/nf-dxgi-idxgifactory-createswapchain), [**IDXGIFactory2:: CreateSwapChainForHwnd**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-createswapchainforhwnd), [**IDXGIFactory2:: CreateSwapChainForCoreWindow**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcorewindow)o [**IDXGIFactory2:: CreateSwapChainForComposition**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcomposition) para describir las opciones de uso de la superficie y de acceso a la CPU para el búfer de reserva de una cadena de intercambio. No puede usar los valores de dxgi uso **\_ \_ compartido**, uso **de dxgi \_ \_ descartar \_ en \_ presente** y **uso de dxgi \_ \_ \_ solo lectura** como entrada para crear una cadena de intercambio. Sin embargo, DXGI puede **establecer \_ \_ descartar el uso \_ de dxgi en \_ presencia** y **uso de dxgi de \_ \_ \_ solo lectura** para algunos de los búferes de reserva de la cadena de intercambio en nombre de la aplicación. Puede llamar al método [**IDXGIResource:: GetUsage**](/windows/desktop/api/DXGI/nf-dxgi-idxgiresource-getusage) para recuperar el uso de estos búferes de reserva. La cadena de intercambio solo admite el valor NONE de acceso de CPU de dxgi en la parte del **campo de acceso de CPU de dxgi \_ \_ \_** del **\_ uso de dxgi**. **\_ \_ \_**

Estas opciones de marca también se usan en el método [**IDXGIDevice:: CreateSurface**](/windows/desktop/api/DXGI/nf-dxgi-idxgidevice-createsurface) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-----------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>DXGI. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Constantes de DXGI](d3d10-graphics-reference-dxgi-constants.md)
</dt> </dl>

 

 




