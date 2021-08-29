---
description: Además de la cadena de intercambio que es propiedad y manipulada a través de la interfaz IDirect3DDevice9, una aplicación puede crear cadenas de intercambio adicionales para presentar varias vistas desde el mismo dispositivo.
ms.assetid: 4fc09b9c-7adb-4f5d-80e0-2d39bc10420e
title: Presentación de varias vistas en modo de ventana (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f43dbbbb300b8ec095593dc3eae1426487fd354a578460f03eb1025ee1a5568b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120095595"
---
# <a name="presenting-multiple-views-in-windowed-mode-direct3d-9"></a>Presentación de varias vistas en modo de ventana (Direct3D 9)

Además de la cadena de intercambio que es propiedad y manipulada a través de la interfaz [**IDirect3DDevice9,**](/windows/desktop/api) una aplicación puede crear cadenas de intercambio adicionales para presentar varias vistas desde el mismo dispositivo. Normalmente, la aplicación crea una cadena de intercambio por vista mediante el método [**IDirect3DDevice9::CreateAdditionalSwapChain**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createadditionalswapchain) y asocia cada cadena de intercambio a una ventana determinada. La aplicación representa imágenes en los búferes de reserva de cada cadena de intercambio y, a continuación, las presenta individualmente.

Solo una cadena de intercambio a la vez puede ser de pantalla completa en cada adaptador.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Programación Sugerencias](programming-tips.md)
</dt> </dl>

 

 
