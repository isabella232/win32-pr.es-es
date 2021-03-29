---
description: Como con cualquier característica, es posible que el controlador que utiliza la aplicación no admita todos los tipos de almacenamiento en búfer de profundidad.
ms.assetid: 8bf022f6-fd97-43f5-ac19-6a75ddb45f5e
title: Consultar la compatibilidad de búfer de profundidad (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bfe7555c1fa0fccddcfcb12ff8bc53f1a0f5f81
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103805293"
---
# <a name="querying-for-depth-buffer-support-direct3d-9"></a>Consultar la compatibilidad de búfer de profundidad (Direct3D 9)

Como con cualquier característica, es posible que el controlador que utiliza la aplicación no admita todos los tipos de almacenamiento en búfer de profundidad. Compruebe siempre las capacidades del controlador. Aunque la mayoría de los controladores admiten el almacenamiento en búfer de profundidad basado en z, no todos admiten el almacenamiento en búfer de profundidad basado en w. Los controladores no producen errores si intenta habilitar un esquema no compatible. En su lugar, revierten a otro método de almacenamiento en búfer de profundidad o deshabilitan el almacenamiento en búfer de profundidad por completo, lo que puede dar lugar a que las escenas se representen con artefactos extremos de ordenación de profundidad.

Puede comprobar la compatibilidad general con los búferes de profundidad consultando en Direct3D el dispositivo de pantalla que utilizará la aplicación antes de crear un dispositivo Direct3D. Si el objeto de Direct3D informa de que admite el almacenamiento en búfer de profundidad, los dispositivos de hardware que cree a partir de este objeto de Direct3D serán compatibles con el almacenamiento en búfer z.

Para consultar la compatibilidad con el almacenamiento en búfer de profundidad, puede usar el método [**IDirect3D9:: CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) , como se muestra en el ejemplo de código siguiente.


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



[**IDirect3D9:: CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) permite elegir un dispositivo para crearlo en función de las capacidades de dicho dispositivo. En este caso, se rechazan los dispositivos que no admiten búferes de profundidad de 16 bits.

En el siguiente ejemplo de código se muestra el uso de [**IDirect3D9:: CheckDepthStencilMatch**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdepthstencilmatch) para determinar la compatibilidad de la galería de símbolos de profundidad con un destino de representación.


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



Cuando sepa que el controlador admite búferes de profundidad, puede comprobar la compatibilidad con el búfer w. Aunque los búferes de profundidad se admiten para todos los rasterizadores de software, los búferes de w solo se admiten en el rasterizador de referencia, que no es adecuado para su uso por parte de aplicaciones del mundo real. Independientemente del tipo de dispositivo que use la aplicación, Compruebe la compatibilidad con búferes w antes de intentar habilitar el almacenamiento en búfer de profundidad basado en w.

1.  Después de crear el dispositivo, llame al método [**IDirect3DDevice9:: GetDeviceCaps**](/windows/desktop/api) , pasando una estructura [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) inicializada.
2.  Después de la llamada, el miembro LineCaps contiene información sobre la compatibilidad del controlador con la representación de primitivas.
3.  Si el miembro RasterCaps de esta estructura contiene la \_ marca D3DPRASTERCAPS WBUFFER, el controlador admite el almacenamiento en búfer de profundidad basado en w para ese tipo primitivo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Búferes de profundidad](depth-buffers.md)
</dt> </dl>

 

 
