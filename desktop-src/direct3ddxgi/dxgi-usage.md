---
description: Marcas para las opciones de creación de recursos y superficies.
ms.assetid: b5026566-89b5-458e-b36d-a55e5f8c10c1
title: DXGI_USAGE (DXGI.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d7bc0773794c6c2243d8a3171cbd6ffdafbe1cdd558e1198c2c8cc0b1a3440d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117909936"
---
# <a name="dxgi_usage"></a>USO DE \_ DXGI

Marcas para las opciones de creación de recursos y superficies.



| Constante o valor                                                                                                                                                                                                                                                                                  | Descripción                                                                                                                                                                                                                                                                                                                     |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DXGI_USAGE_BACK_BUFFER"></span><span id="dxgi_usage_back_buffer"></span><dl> <dt>**DXGI \_ BÚFER \_ DE \_ RESERVA DE**</dt> USO <dt>1L << (2 + 4)</dt> </dl>                             | La superficie o el recurso se usa como búfer de reserva. No es necesario pasar **DXGI \_ USAGE BACK \_ \_ BUFFER** al crear una cadena de intercambio. Pero puede determinar si un recurso pertenece a una cadena de intercambio al llamar a [**IDXGIResource::GetUsage**](/windows/desktop/api/DXGI/nf-dxgi-idxgiresource-getusage) y obtener **DXGI \_ USAGE BACK \_ \_ BUFFER**.<br/> |
| <span id="DXGI_USAGE_DISCARD_ON_PRESENT"></span><span id="dxgi_usage_discard_on_present"></span><dl> <dt>**DXGI \_ DESCARTE \_ DE USO EN \_ \_ LA**</dt> <dt> <<  1L (5 + 4)</dt> </dl>       | Esta marca es solo para uso interno.<br/>                                                                                                                                                                                                                                                                                  |
| <span id="DXGI_USAGE_READ_ONLY"></span><span id="dxgi_usage_read_only"></span><dl> <dt>**DXGI \_ USAGE \_ READ \_ ONLY**</dt> <dt>1L << (4 + 4)</dt> </dl>                                   | Use la superficie o el recurso solo para leer.<br/>                                                                                                                                                                                                                                                                        |
| <span id="DXGI_USAGE_RENDER_TARGET_OUTPUT"></span><span id="dxgi_usage_render_target_output"></span><dl> <dt>**DXGI \_ USAGE \_ RENDER \_ TARGET \_ OUTPUT**</dt> <dt>1L << (1 + 4)</dt> </dl> | Use la superficie o el recurso como destino de representación de salida.<br/>                                                                                                                                                                                                                                                              |
| <span id="DXGI_USAGE_SHADER_INPUT"></span><span id="dxgi_usage_shader_input"></span><dl> <dt>**DXGI \_ ENTRADA \_ DEL \_ SOMBREADOR DE**</dt> USO <dt>1L << (0 + 4)</dt> </dl>                          | Use la superficie o el recurso como entrada para un sombreador.<br/>                                                                                                                                                                                                                                                                 |
| <span id="DXGI_USAGE_SHARED"></span><span id="dxgi_usage_shared"></span><dl> <dt>**DXGI \_ USO \_ COMPARTIDO**</dt> <dt>1L << (3 + 4)</dt> </dl>                                             | Comparta la superficie o el recurso.<br/>                                                                                                                                                                                                                                                                                       |
| <span id="DXGI_USAGE_UNORDERED_ACCESS"></span><span id="dxgi_usage_unordered_access"></span><dl> <dt>**DXGI \_ ACCESO \_ SIN ORDENAR DE \_ USO**</dt> <dt>1L << (6 + 4)</dt> </dl>              | Use la superficie o el recurso para el acceso desordenado.<br/>                                                                                                                                                                                                                                                                    |



## <a name="remarks"></a>Comentarios

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

Estas opciones de marca se usan en una llamada al método [**IDXGIFactory::CreateSwapChain**](/windows/desktop/api/DXGI/nf-dxgi-idxgifactory-createswapchain), [**IDXGIFactory2::CreateSwapChainForHwnd**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-createswapchainforhwnd), [**IDXGIFactory2::CreateSwapChainForCoreWindow**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcorewindow)o [**IDXGIFactory2::CreateSwapChainForComposition**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcomposition) para describir el uso de la superficie y las opciones de acceso de CPU para el búfer de reserva de una cadena de intercambio. No puede usar los valores **DXGI \_ USAGE \_ SHARED**, **DXGI \_ USAGE DISCARD \_ ON \_ \_ PRESENT** y **DXGI USAGE READ \_ \_ \_ ONLY** como entrada para crear una cadena de intercambio. Sin embargo, DXGI puede establecer **DXGI \_ USAGE DISCARD \_ ON \_ \_ PRESENT** y **DXGI USAGE READ \_ \_ \_ ONLY** para algunos de los búferes de reserva de la cadena de intercambio en nombre de la aplicación. Puede llamar al método [**IDXGIResource::GetUsage**](/windows/desktop/api/DXGI/nf-dxgi-idxgiresource-getusage) para recuperar el uso de estos búferes de reserva. La cadena de intercambio solo admite el valor **DXGI \_ CPU ACCESS \_ \_ NONE** en la **parte DXGI CPU ACCESS \_ \_ \_ FIELD** de **DXGI \_ USAGE**.

El método [**IDXGIDevice::CreateSurface**](/windows/desktop/api/DXGI/nf-dxgi-idxgidevice-createsurface) también usa estas opciones de marca.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-----------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>DXGI.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Constantes DXGI](d3d10-graphics-reference-dxgi-constants.md)
</dt> </dl>

 

 




