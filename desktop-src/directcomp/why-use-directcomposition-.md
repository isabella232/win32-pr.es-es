---
title: Por qué usar DirectComposition
description: En este tema se describen las capacidades y ventajas de Microsoft DirectComposition.
ms.assetid: D597E737-24A1-49E9-8861-9DDD6D7FF2F8
keywords:
- Por qué usar DirectComposition
- razones para usar DirectComposition
- Funcionalidades y ventajas de DirectComposition
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7ad68f779abc023b7645ed9e66f8af3bf63a140
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105695718"
---
# <a name="why-use-directcomposition"></a>¿Por qué usar DirectComposition?

> [!NOTE]
> En el caso de las aplicaciones de Windows 10, se recomienda usar las API de Windows. UI. Composition en lugar de DirectComposition. Para obtener más información, consulte [modernice su aplicación de escritorio con el nivel de objetos visuales](/windows/uwp/composition/visual-layer-in-desktop-apps).

En este tema se describen las capacidades y ventajas de Microsoft DirectComposition. Contiene las secciones siguientes:

-   [Crear una interfaz de usuario visualmente atractiva](#create-a-visually-engaging-user-interface)
-   [Habilitar animaciones enriquecidas y suaves para la aplicación](#enable-rich-smooth-animations-for-your-application)
-   [Combinar mapas de bits de diversos orígenes](#combine-bitmaps-from-a-variety-of-sources)
-   [Ahorro de memoria mediante la integración con DWM](#memory-savings-though-integration-with-dwm)
-   [Mantenga lo que ya tiene](#keep-what-you-already-have)
-   [Temas relacionados](#related-topics)

## <a name="create-a-visually-engaging-user-interface"></a>Crear una interfaz de usuario visualmente atractiva

DirectComposition permite combinar y animar [*objetos visuales*](directcomposition-glossary.md) para crear una interfaz de usuario visualmente atractiva para las aplicaciones basadas en Windows. Puede ayudar a dar a la aplicación una apariencia única y establecer una identidad que se aparte de otras aplicaciones.

DirectComposition también puede ayudar a facilitar el uso de sus aplicaciones. Por ejemplo, puedes utilizarlo para crear indicaciones visuales y transiciones de pantalla animadas que muestren las relaciones entre los elementos de la pantalla.

## <a name="enable-rich-smooth-animations-for-your-application"></a>Habilitar animaciones enriquecidas y suaves para la aplicación

DirectComposition es un motor de composición de mapas de bits de alto rendimiento que usa gráficos acelerados por hardware para lograr velocidades de fotogramas altas, lo que produce una panorámica, un desplazamiento y animaciones de contenido complejo suaves y coherentes. Dado que funciona en un subproceso dedicado que es independiente del subproceso utilizado para representar la interfaz de usuario de la aplicación, DirectComposition nunca puede "privar" el subproceso de la interfaz de usuario ni interferir con la capacidad de la aplicación para dibujar sus elementos de la interfaz de usuario.

## <a name="combine-bitmaps-from-a-variety-of-sources"></a>Combinar mapas de bits de diversos orígenes

Muchas aplicaciones basadas en Windows tienen una interfaz de usuario formada por elementos creados por una variedad de marcos de gráficos diferentes. Por ejemplo, una aplicación podría usar Windows Forms para crear una barra de estado, Windows Interfaz de dispositivo gráfico (GDI) para crear el contenido de la ventana principal, el contenido de Microsoft DirectX para gráficos, etc. DirectComposition permite combinar el contenido de una variedad de marcos de gráficos y hacer que se represente en la misma ventana secundaria o de nivel superior sin necesidad de preocuparse de lo que sucede si se superpone el contenido de marcos de trabajo diferentes.

## <a name="memory-savings-though-integration-with-dwm"></a>Ahorro de memoria mediante la integración con DWM

Las composiciones y animaciones creadas por DirectComposition se pasan a un componente integrado de Windows llamado [Administrador de ventanas de escritorio (DWM)](/windows/desktop/dwm/dwm-overview) para la representación en pantalla. Por lo tanto, no se requieren componentes de representación especiales ni marcos de interfaz de usuario en el equipo.

## <a name="keep-what-you-already-have"></a>Mantenga lo que ya tiene

El código de la interfaz de usuario de una aplicación existente basada en Windows representa una inversión significativa. En su mayor parte, DirectComposition le permite crear y animar el contenido de la interfaz de usuario existente. Esto significa que puede usar DirectComposition para realizar actualizaciones y mejoras importantes en la interfaz de usuario de la aplicación sin necesidad de realizar cambios significativos en la base de código de interfaz de usuario existente.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[DirectComposition](directcomposition-portal.md)
</dt> </dl>

 

 