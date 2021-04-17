---
description: Opciones para enumerar los modos de presentación.
ms.assetid: 7e0f5629-f8e2-478b-b8eb-00780a3dcf1f
title: DXGI_ENUM_MODES (DXGI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 056ad959f0b86fb6f357d690f2daab908275e038
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105670222"
---
# <a name="dxgi_enum_modes"></a>\_modos de enumeración de DXGI \_

Opciones para enumerar los modos de presentación.



| Constante o valor                                                                                                                                                                                                                                                                  | Descripción                                                                                                                                                                                                                                                                                                                                     |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DXGI_ENUM_MODES_INTERLACED"></span><span id="dxgi_enum_modes_interlaced"></span><dl> <dt>**DXGI \_ Modos de ENUMERAción \_ \_ entrelazados**</dt> <dt>1UL</dt> </dl>                 | Incluye modos entrelazados.<br/>                                                                                                                                                                                                                                                                                                            |
| <span id="DXGI_ENUM_MODES_SCALING"></span><span id="dxgi_enum_modes_scaling"></span><dl> <dt>**DXGI \_ Modos de ENUMERAción \_ \_ escala**</dt> <dt>2UL</dt> </dl>                          | Incluye modos de escalado elástico.<br/>                                                                                                                                                                                                                                                                                                     |
| <span id="DXGI_ENUM_MODES_STEREO"></span><span id="dxgi_enum_modes_stereo"></span><dl> <dt>**DXGI \_ Modos de ENUMERAción \_ \_ estéreo**</dt> <dt>4UL</dt> </dl>                             | Incluye modos estereofónicos.<br/> **Direct3D 11:** Este valor de enumeración se admite a partir de Windows 8.<br/>                                                                                                                                                                                                                       |
| <span id="DXGI_ENUM_MODES_DISABLED_STEREO"></span><span id="dxgi_enum_modes_disabled_stereo"></span><dl> <dt>**DXGI \_ Modos de ENUMERAción 8UL \_ \_ \_ estéreo deshabilitados**</dt> <dt></dt> </dl> | Incluye modos estereofónicos que están ocultos porque el usuario ha deshabilitado el estéreo. Las aplicaciones del panel de control pueden usar esta opción para mostrar las capacidades de estéreo que se han deshabilitado como parte de una interfaz de usuario que habilita y deshabilita el estéreo.<br/> **Direct3D 11:** Este valor de enumeración se admite a partir de Windows 8.<br/> |



## <a name="remarks"></a>Observaciones

Estas opciones de marca se usan en [**IDXGIOutput:: GetDisplayModeList**](/windows/desktop/api/DXGI/nf-dxgi-idxgioutput-getdisplaymodelist) para enumerar los modos de presentación.

Estas opciones de marca también se usan en [**IDXGIOutput1:: GetDisplayModeList1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutput1-getdisplaymodelist1) para enumerar los modos de presentación.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-----------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>DXGI. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Constantes de DXGI](d3d10-graphics-reference-dxgi-constants.md)
</dt> </dl>

 

 




