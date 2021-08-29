---
description: Como con cualquier característica, es posible que el controlador que usa la aplicación no admita todos los tipos de almacenamiento en búfer de profundidad.
ms.assetid: 8bf022f6-fd97-43f5-ac19-6a75ddb45f5e
title: Consulta de compatibilidad con búfer de profundidad (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1050edc61e5359cca0ac9c2990d35f27c8c8db6b193d219f928ac336e99d760
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120118585"
---
# <a name="querying-for-depth-buffer-support-direct3d-9"></a>Consulta de compatibilidad con búfer de profundidad (Direct3D 9)

Como con cualquier característica, es posible que el controlador que usa la aplicación no admita todos los tipos de almacenamiento en búfer de profundidad. Compruebe siempre las funcionalidades del controlador. Aunque la mayoría de los controladores admiten el almacenamiento en búfer de profundidad basado en z, no todos admitirán el almacenamiento en búfer de profundidad basado en w. Los controladores no producirán errores si intenta habilitar un esquema no admitido. En su lugar, se reservan en otro método de almacenamiento en búfer de profundidad o, a veces, deshabilitan el almacenamiento en búfer de profundidad por completo, lo que puede dar lugar a escenas que se representan con artefactos de ordenación de profundidad extremos.

Para comprobar la compatibilidad general con los búferes de profundidad, consulte Direct3D para el dispositivo de visualización que la aplicación usará antes de crear un dispositivo Direct3D. Si el objeto Direct3D informa de que admite el almacenamiento en búfer de profundidad, los dispositivos de hardware que cree a partir de este objeto direct3D admitirán el almacenamiento en búfer z.

Para consultar la compatibilidad con el almacenamiento en búfer de profundidad, puede usar el método [**IDirect3D9::CheckDeviceFormat,**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) como se muestra en el ejemplo de código siguiente.


```
// The following example assumes that pCaps is a valid pointer to an 
// initialized D3DCAPS9 structure
if(FAILED(m_pD3D->CheckDeviceFormat(pCaps->AdapterOrdinal, 
                                    pCaps->DeviceType, 
                                    AdapterFormat, 
                                    D3DUSAGE_DEPTHSTENCIL, 
                                    D3DRTYPE_SURFACE,
                                    D3DFMT_D16)))
    return E_FAIL;
```



[**IDirect3D9::CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) permite elegir un dispositivo para crear en función de las funcionalidades de ese dispositivo. En este caso, se rechazan los dispositivos que no admiten búferes de profundidad de 16 bits.

El [**uso de IDirect3D9::CheckDepthStencilMatch para**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdepthstencilmatch) determinar la compatibilidad de la galería de símbolos de profundidad con un destino de representación se muestra en el ejemplo de código siguiente.


```
// Reject devices that cannot create a render target of RTFormat while
// the back buffer is of RTFormat and the depth-stencil buffer is
// at least 8 bits of stencil
if(FAILED(m_pD3D->CheckDepthStencilMatch(pCaps->AdapterOrdinal,
                                        pCaps->DeviceType, 
                                        AdapterFormat, 
                                        RTFormat, 
                                        D3DFMT_D24S8)))
    return E_FAIL;
```



Cuando sepa que el controlador admite búferes de profundidad, puede comprobar la compatibilidad con w-buffer. Aunque los búferes de profundidad se admiten para todos los rasterizadores de software, w-buffers solo son compatibles con el rasterizador de referencia, que no es adecuado para su uso por aplicaciones del mundo real. Independientemente del tipo de dispositivo que use la aplicación, compruebe la compatibilidad con w-buffers antes de intentar habilitar el almacenamiento en búfer de profundidad basado en w.

1.  Después de crear el dispositivo, llame al método [**IDirect3DDevice9::GetDeviceCaps**](/windows/desktop/api) y pase una estructura [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) inicializada.
2.  Después de la llamada, el miembro LineCaps contiene información sobre la compatibilidad del controlador para representar primitivas.
3.  Si el miembro RasterCaps de esta estructura contiene la marca WBUFFER D3DPRASTERCAPS, el controlador admite el almacenamiento en búfer de profundidad basado en w para \_ ese tipo primitivo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Búferes de profundidad](depth-buffers.md)
</dt> </dl>

 

 
