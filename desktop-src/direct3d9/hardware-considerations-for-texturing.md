---
description: El hardware actual no implementa necesariamente toda la funcionalidad que la interfaz Direct3D habilita. La aplicación debe probar el hardware del usuario y ajustar sus estrategias de representación en consecuencia.
ms.assetid: 7b5f586c-616c-4351-b6b9-5c0179db5d8b
title: Consideraciones de hardware para la texturización (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21f1ba8bea85cc3657478767aac7c7ffc2abebbd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103906292"
---
# <a name="hardware-considerations-for-texturing-direct3d-9"></a>Consideraciones de hardware para la texturización (Direct3D 9)

El hardware actual no implementa necesariamente toda la funcionalidad que la interfaz Direct3D habilita. La aplicación debe probar el hardware del usuario y ajustar sus estrategias de representación en consecuencia.

Muchas tarjetas aceleradoras 3D no admiten valores iterados difusos como argumentos para las unidades de mezcla. Sin embargo, la aplicación puede introducir datos de color iterados cuando realiza la combinación de texturas.

Es posible que algún hardware 3D no tenga una fase de fusión asociada a la primera textura. En estos adaptadores, la aplicación debe realizar la combinación en la segunda y tercera fase de textura en el conjunto de texturas actuales.

Debido a las limitaciones de gran parte del hardware de hoy en día, algunos adaptadores de pantalla pueden realizar la interpolación de mipmap trilineal a través de la interfaz de combinación de texturas múltiple ofrecida por [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9). La aplicación puede utilizar la combinación de texturas de Multipass para lograr los mismos efectos, o bien degradarse al \_ modo de filtro MIP del punto de D3DTEXF, que es ampliamente compatible.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Texturas de Direct3D](direct3d-textures.md)
</dt> </dl>

 

 
