---
title: Por qué usar DirectComposition
description: En este tema se describen las funcionalidades y ventajas de Microsoft DirectComposition.
ms.assetid: D597E737-24A1-49E9-8861-9DDD6D7FF2F8
keywords:
- Por qué usar DirectComposition
- razones para usar DirectComposition
- Funcionalidades y ventajas de DirectComposition
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe9b67b17869c53b393d8a1f1ecb6230a69322d898f691c21370a5b24befda21
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119562095"
---
# <a name="why-use-directcomposition"></a>¿Por qué usar DirectComposition?

> [!NOTE]
> Para las aplicaciones Windows 10, se recomienda usar Windows.UI.Composition API en lugar de DirectComposition. Para obtener más información, [consulte Modernización de la aplicación de escritorio mediante la capa visual](/windows/uwp/composition/visual-layer-in-desktop-apps).

En este tema se describen las funcionalidades y ventajas de Microsoft DirectComposition. Contiene las secciones siguientes:

-   [Creación de una interfaz de usuario visualmente atractiva](#create-a-visually-engaging-user-interface)
-   [Habilitación de animaciones fluidas y enriquecciones para la aplicación](#enable-rich-smooth-animations-for-your-application)
-   [Combinación de mapas de bits de una variedad de orígenes](#combine-bitmaps-from-a-variety-of-sources)
-   [Ahorro de memoria a través de la integración con DWM](#memory-savings-though-integration-with-dwm)
-   [Conservar lo que ya tiene](#keep-what-you-already-have)
-   [Temas relacionados](#related-topics)

## <a name="create-a-visually-engaging-user-interface"></a>Creación de una interfaz de usuario visualmente atractiva

DirectComposition permite combinar y animar [*objetos visuales*](directcomposition-glossary.md) para crear una interfaz de usuario visualmente atractiva para las Windows basadas en aplicaciones. Puede ayudar a dar a la aplicación una apariencia única, estableciendo una identidad que la diferencia de otras aplicaciones.

DirectComposition también puede ayudar a facilitar el uso de las aplicaciones. Por ejemplo, puedes utilizarlo para crear indicaciones visuales y transiciones de pantalla animadas que muestren las relaciones entre los elementos de la pantalla.

## <a name="enable-rich-smooth-animations-for-your-application"></a>Habilitación de animaciones fluidas y enriquecciones para la aplicación

DirectComposition es un motor de composición de mapa de bits de alto rendimiento que usa gráficos acelerados por hardware para lograr velocidades de fotogramas altas, lo que da lugar a un movimiento panorámico, desplazamiento y animaciones uniformes y uniformes de contenido complejo. Dado que funciona en un subproceso dedicado que es independiente del subproceso que se usa para representar la interfaz de usuario de la aplicación, DirectComposition nunca puede "estrellar" el subproceso de interfaz de usuario ni interferir con la capacidad de la aplicación para dibujar sus elementos de interfaz de usuario.

## <a name="combine-bitmaps-from-a-variety-of-sources"></a>Combinación de mapas de bits de una variedad de orígenes

Muchas Windows basadas en gráficos tienen una interfaz de usuario que consta de elementos creados por una variedad de marcos de gráficos diferentes. Por ejemplo, una aplicación podría usar Windows Forms para crear una barra de estado, Windows Interfaz de dispositivo gráfico (GDI) para crear el contenido de la ventana principal, Microsoft DirectX para el contenido gráfico, y así sucesivamente. DirectComposition permite combinar el contenido de una variedad de marcos de gráficos y hacer que se represente en la misma ventana de nivel superior o secundario sin necesidad de preocuparse por lo que sucede si el contenido de diferentes marcos se superpone.

## <a name="memory-savings-though-integration-with-dwm"></a>Ahorro de memoria a través de la integración con DWM

Las composiciones y animaciones creadas por DirectComposition se pasan a un componente integrado de Windows denominado [Administrador de ventanas de escritorio (DWM)](/windows/desktop/dwm/dwm-overview) para la representación en la pantalla. Por lo tanto, no se requiere ningún componente de representación especial ni marcos de interfaz de usuario en el equipo.

## <a name="keep-what-you-already-have"></a>Conservar lo que ya tiene

El código de interfaz de usuario de una aplicación Windows basada en datos existente representa una inversión significativa. En su mayor parte, DirectComposition permite crear y animar el contenido de la interfaz de usuario existente. Esto significa que puede usar DirectComposition para realizar actualizaciones y mejoras significativas en la interfaz de usuario de la aplicación sin necesidad de realizar cambios exhaustivos en la base de código de la interfaz de usuario existente.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[DirectComposition](directcomposition-portal.md)
</dt> </dl>

 

 