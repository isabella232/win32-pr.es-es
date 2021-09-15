---
description: El hardware actual no implementa necesariamente toda la funcionalidad que habilita la interfaz de Direct3D. La aplicación debe probar el hardware del usuario y ajustar sus estrategias de representación en consecuencia.
ms.assetid: 7b5f586c-616c-4351-b6b9-5c0179db5d8b
title: Consideraciones de hardware para texturing (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21f1ba8bea85cc3657478767aac7c7ffc2abebbd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127465378"
---
# <a name="hardware-considerations-for-texturing-direct3d-9"></a>Consideraciones de hardware para texturing (Direct3D 9)

El hardware actual no implementa necesariamente toda la funcionalidad que habilita la interfaz de Direct3D. La aplicación debe probar el hardware del usuario y ajustar sus estrategias de representación en consecuencia.

Muchas tarjetas de acelerador 3D no admiten valores iterados difusos como argumentos para combinar unidades. Sin embargo, la aplicación puede introducir datos de color iterados cuando realiza la combinación de texturas.

Es posible que algún hardware 3D no tenga una fase de mezcla asociada a la primera textura. En estos adaptadores, la aplicación debe realizar la combinación en la segunda y tercera fases de textura del conjunto de texturas actuales.

Debido a las limitaciones de gran parte del hardware actual, pocos adaptadores de pantalla pueden realizar la interpolación de mapas mip trilinear a través de la interfaz de mezcla de texturas múltiple que ofrece [**IDirect3DDevice9.**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) La aplicación puede usar la mezcla de textura multipass para lograr los mismos efectos o degradar al modo de filtro mipmap de D3DTEXF POINT, que es ampliamente \_ compatible.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Texturas de Direct3D](direct3d-textures.md)
</dt> </dl>

 

 
