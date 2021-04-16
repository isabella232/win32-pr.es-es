---
description: Además de la cadena de intercambio que posee y manipula a través de la interfaz IDirect3DDevice9, una aplicación puede crear cadenas de intercambio adicionales para presentar varias vistas del mismo dispositivo.
ms.assetid: 4fc09b9c-7adb-4f5d-80e0-2d39bc10420e
title: Presentar varias vistas en modo de ventana (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 039b02c487e06c7464dc8163c719371dc2b23706
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104538229"
---
# <a name="presenting-multiple-views-in-windowed-mode-direct3d-9"></a>Presentar varias vistas en modo de ventana (Direct3D 9)

Además de la cadena de intercambio que posee y manipula a través de la interfaz [**IDirect3DDevice9**](/windows/desktop/api) , una aplicación puede crear cadenas de intercambio adicionales para presentar varias vistas del mismo dispositivo. Normalmente, la aplicación crea una cadena de intercambio por cada vista mediante el método [**IDirect3DDevice9:: CreateAdditionalSwapChain**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createadditionalswapchain) y asocia cada cadena de intercambio a una ventana determinada. La aplicación representa las imágenes en los búferes de reserva de cada cadena de intercambio y, a continuación, las presenta individualmente.

Solo una cadena de intercambio a la vez puede estar en pantalla completa en cada adaptador.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Sugerencias de programación](programming-tips.md)
</dt> </dl>

 

 
