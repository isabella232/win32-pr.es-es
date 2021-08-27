---
description: Opciones para enumerar los modos de presentación.
ms.assetid: 7e0f5629-f8e2-478b-b8eb-00780a3dcf1f
title: DXGI_ENUM_MODES (DXGI.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 568e3919955c2f5612cf88896a2cb6389ebc58fcb427e159824c1dc2feeebca6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120025635"
---
# <a name="dxgi_enum_modes"></a>MODOS DE \_ ENUMERACIÓN DXGI \_

Opciones para enumerar los modos de presentación.



| Constante o valor                                                                                                                                                                                                                                                                  | Descripción                                                                                                                                                                                                                                                                                                                                     |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DXGI_ENUM_MODES_INTERLACED"></span><span id="dxgi_enum_modes_interlaced"></span><dl> <dt>**DXGI \_ MODOS DE \_ \_ ENUMERACIÓN ENTRELAZADOS**</dt> <dt>1UL</dt> </dl>                 | Incluir modos entrelazados.<br/>                                                                                                                                                                                                                                                                                                            |
| <span id="DXGI_ENUM_MODES_SCALING"></span><span id="dxgi_enum_modes_scaling"></span><dl> <dt>**DXGI \_ MODOS DE \_ ENUMERACIÓN \_ ESCALADO**</dt> <dt>2UL</dt> </dl>                          | Incluir modos de escalado extendido.<br/>                                                                                                                                                                                                                                                                                                     |
| <span id="DXGI_ENUM_MODES_STEREO"></span><span id="dxgi_enum_modes_stereo"></span><dl> <dt>**DXGI \_ MODOS DE \_ \_ ENUMERACIÓN ESTÉREO**</dt> <dt>4UL</dt> </dl>                             | Incluir modos estéreo.<br/> **Direct3D 11:** Este valor de enumeración se admite a partir de Windows 8.<br/>                                                                                                                                                                                                                       |
| <span id="DXGI_ENUM_MODES_DISABLED_STEREO"></span><span id="dxgi_enum_modes_disabled_stereo"></span><dl> <dt>**DXGI \_ MODOS DE \_ ENUMERACIÓN \_ \_ DESHABILITADOS ESTÉREO**</dt> <dt>8UL</dt> </dl> | Incluya modos estéreo que estén ocultos porque el usuario ha deshabilitado el estéreo. Las aplicaciones del panel de control pueden usar esta opción para mostrar las funcionalidades estéreo que se han deshabilitado como parte de una interfaz de usuario que habilita y deshabilita estéreo.<br/> **Direct3D 11:** Este valor de enumeración se admite a partir de Windows 8.<br/> |



## <a name="remarks"></a>Comentarios

Estas opciones de marca se usan [**en IDXGIOutput::GetDisplayModeList**](/windows/desktop/api/DXGI/nf-dxgi-idxgioutput-getdisplaymodelist) para enumerar los modos de presentación.

Estas opciones de marca también se usan en [**IDXGIOutput1::GetDisplayModeList1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutput1-getdisplaymodelist1) para enumerar los modos de presentación.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-----------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>DXGI.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Constantes DXGI](d3d10-graphics-reference-dxgi-constants.md)
</dt> </dl>

 

 




