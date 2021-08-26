---
description: Además de la cadena de intercambio propiedad y manipulada a través del objeto Direct3DDevice, una aplicación puede usar el método IDirect3DDevice9::CreateAdditionalSwapChain para crear cadenas de intercambio adicionales para presentar varias vistas desde el mismo dispositivo.
ms.assetid: f0d01dfb-d1de-4d16-8c64-4ae56d7fed06
title: Varias vistas en modo de ventana (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e2784a4f2bd855293e427aa9297d2e5725a74a3f5bce52b4b53cdf3d9081062
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120069025"
---
# <a name="multiple-views-in-windowed-mode-direct3d-9"></a>Varias vistas en modo de ventana (Direct3D 9)

Además de la cadena de intercambio propiedad y manipulada a través del objeto Direct3DDevice, una aplicación puede usar el método [**IDirect3DDevice9::CreateAdditionalSwapChain**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createadditionalswapchain) para crear cadenas de intercambio adicionales para presentar varias vistas desde el mismo dispositivo.

Normalmente, la aplicación crea una cadena de intercambio por vista y asocia cada cadena de intercambio a una vista determinada. La aplicación representa imágenes en los búferes de reserva de cada cadena de intercambio y, a continuación, usa el método [**IDirect3DDevice9::P resent**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) para presentarlas individualmente. Tenga en cuenta que solo una cadena de intercambio a la vez puede ser de pantalla completa en cada adaptador.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Presentación de una escena](presenting-a-scene.md)
</dt> </dl>

 

 
