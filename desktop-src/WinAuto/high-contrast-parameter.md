---
title: Parámetro de contraste alto
description: El parámetro de contraste alto indica si el usuario desea un contraste alto entre los colores usados para los objetos visuales de primer plano y de fondo.
ms.assetid: ec89c4ce-4e8b-4e1f-a349-fbd47431d675
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f1255e8a99b3cb253146e2fa2c019a879c4a1b6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103995388"
---
# <a name="high-contrast-parameter"></a>Parámetro de contraste alto

El parámetro de contraste alto indica si el usuario desea un contraste alto entre los colores usados para los objetos visuales de primer plano y de fondo.

El usuario controla el valor del parámetro de contraste alto mediante el centro de accesibilidad del panel de control u otra aplicación para personalizar el entorno. Las aplicaciones usan las marcas **SPI \_ GETHIGHCONTRAST** y **SPI \_ SETHIGHCONTRAST** con la función [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) para obtener y establecer el parámetro de contraste alto.

Durante la inicialización y al procesar los mensajes de [**WM \_ SYSCOLORCHANGE**](/windows/desktop/gdi/wm-syscolorchange) , las aplicaciones deben determinar el estado del parámetro de contraste alto. Para tomar esta determinación, las aplicaciones deben llamar a [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) con la marca **SPI \_ GETHIGHCONTRAST** para obtener una estructura de [**HIGHCONTRAST**](/windows/win32/api/winuser/ns-winuser-highcontrasta) . Si el miembro **dwFlags** de la estructura **HIGHCONTRAST** tiene el conjunto de bits **HCF \_ HIGHCONTRASTON** , se habilita la característica de contraste alto y las aplicaciones deben hacer lo siguiente:

-   Asigna todos los colores a un solo par de colores de primer plano y de fondo. Utilice la función [**GetSysColor**](/windows/desktop/api/winuser/nf-winuser-getsyscolor) para determinar los colores de primer plano y de fondo adecuados, mediante una combinación de **\_ WINDOWTEXT** de color y de **\_ ventana de color** , o bien una combinación de **\_ BTNTEXT de color** y **\_ BTNFACE de color**. La función **GetSysColor** devuelve los colores seleccionados por el usuario a través del panel de control.
-   Omitir cualquier imagen de mapa de imágenes que normalmente se mostraría detrás del texto. Estas imágenes distraen visualmente a un usuario que necesita contraste alto.
-   Las imágenes que normalmente se dibujarían en varios colores deben dibujarse con los colores de primer plano y de fondo seleccionados para el texto.

Además, las aplicaciones usan las marcas **SPI \_ GETDISABLEOVERLAPPEDCONTENT** y **SPI \_ SETDISABLEOVERLAPPEDCONTENT** con la función [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) para obtener y establecer el parámetro de contenido superpuesto. Mostrar características como imágenes de fondo, fondos con textura, marcas de agua en documentos, combinación alfa y transparencia puede reducir el contraste entre el primer plano y el fondo, lo que dificulta a los usuarios con deficiencias visuales ver los objetos de la pantalla. Esta marca permite a las aplicaciones determinar si se ha deshabilitado dicho contenido superpuesto

 

 