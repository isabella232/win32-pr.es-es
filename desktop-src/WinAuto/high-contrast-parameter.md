---
title: Parámetro de contraste alto
description: El parámetro de contraste alto indica si el usuario desea un contraste alto entre los colores usados para los objetos visuales de primer plano y de fondo.
ms.assetid: ec89c4ce-4e8b-4e1f-a349-fbd47431d675
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f1255e8a99b3cb253146e2fa2c019a879c4a1b6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160560"
---
# <a name="high-contrast-parameter"></a>Parámetro de contraste alto

El parámetro de contraste alto indica si el usuario desea un contraste alto entre los colores usados para los objetos visuales de primer plano y de fondo.

El usuario controla la configuración del parámetro de contraste alto mediante el Centro de accesibilidad en Panel de control u otra aplicación para personalizar el entorno. Las aplicaciones usan las marcas **SPI \_ GETHIGHCONTRAST** y **SPI \_ SETHIGHCONTRAST** con la función [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) para obtener y establecer el parámetro de contraste alto.

Durante la inicialización y al procesar [**mensajes \_ SYSCOLORCHANGE de WM,**](/windows/desktop/gdi/wm-syscolorchange) las aplicaciones deben determinar el estado del parámetro de contraste alto. Para realizar esta determinación, las aplicaciones deben llamar a [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) con **la marca SPI \_ GETHIGHCONTRAST** para obtener una [**estructura HIGHCONTRAST.**](/windows/win32/api/winuser/ns-winuser-highcontrasta) Si el **miembro dwFlags** de la estructura **HIGHCONTRAST** tiene el conjunto de bits **\_ HCF HIGHCONTRASTON,** la característica de contraste alto está habilitada y las aplicaciones deben hacer lo siguiente:

-   Asigne todos los colores a un único par de colores de primer plano y de fondo. Use la función [**GetSysColor**](/windows/desktop/api/winuser/nf-winuser-getsyscolor) para determinar los colores de primer plano y fondo adecuados, mediante una combinación de **COLOR \_ WINDOWTEXT** y **COLOR \_ WINDOW** o una combinación de **COLOR \_ BTNTEXT** y **COLOR \_ BTNFACE.** La **función GetSysColor** devuelve los colores seleccionados por el usuario a través del Panel de control.
-   Omita las imágenes de mapa de bits que normalmente se mostrarían detrás del texto. Estas imágenes distraen visualmente a un usuario que necesita contraste alto.
-   Las imágenes que normalmente se dibujarían en varios colores se deben dibujar con los colores de primer plano y de fondo seleccionados para el texto.

Además, las aplicaciones usan las marcas **SPI \_ GETDISABLEOVERLAPPEDCONTENT** y **SPI \_ SETDISABLEOVERLAPPEDCONTENT** con la función [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) para obtener y establecer el parámetro de contenido superpuesto. Mostrar características como imágenes de fondo, fondos con textura, marcas de agua en documentos, combinación alfa y transparencia pueden reducir el contraste entre el primer plano y el fondo, lo que dificulta que los usuarios con visión baja vean objetos en la pantalla. Esta marca permite a las aplicaciones determinar si dicho contenido superpuesto se ha deshabilitado.

 

 