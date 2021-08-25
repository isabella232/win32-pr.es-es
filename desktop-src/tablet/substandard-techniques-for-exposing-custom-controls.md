---
description: Descripción de técnicas no estándar para exponer controles personalizados.
ms.assetid: 107968c6-c3b3-462d-b488-96c69f2b3b14
title: Técnicas no estándar para exponer controles personalizados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 121856bf5303b011b785a26bc47013e0df93463d7f278d6e4586991a47d8e020
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119934315"
---
# <a name="substandard-techniques-for-exposing-custom-controls"></a>Técnicas no estándar para exponer controles personalizados

Si una aplicación no admite Microsoft Active Accessibility, es posible que no sea totalmente accesible. Las técnicas siguientes representan controles parcialmente compatibles:

-   Devuelve una cadena descriptiva cuando se consulta el control mediante el mensaje \_ GETTEXT de WM. Por ejemplo, permita que un equivalente personalizado de un control de botón con la etiqueta "Imprimir" devuelva la cadena "Botón imprimir". Esto identifica el tipo de control y la etiqueta. La misma cadena es adecuada para un botón con una etiqueta que no sea texto, como un gráfico de una impresora. De forma similar, permita que un control personalizado que se comporte como una casilla devuelva la cadena de título "Casilla De impresión habilitada, activada".
-   Admite el mensaje \_ WM GETDLGCODE, que identifica la entrada de teclado que se admite. Por ejemplo, permita que un equivalente personalizado de un control de edición controle WM GETDLGCODE devolviendo DLGC HASSETSEL si controla los mensajes para establecer la \_ selección, DLGC WANTARROWS si usa teclas de dirección y \_ \_ DLGC WANTCHARS para indicar que usa la entrada de \_ caracteres.
    > [!Note]  
    > Solo los controles que tienen sus propios identificadores de ventana pueden responder a los mensajes GETTEXT y \_ WM \_ GETDLGCODE de WM.

     

Para evitar problemas de compatibilidad con las ayuda de accesibilidad, debe seguir Active Accessibility directrices estrechamente al diseñar controles personalizados. Para obtener más información sobre cómo evitar problemas de compatibilidad con las ayuda de accesibilidad, vea la [sección Accesibilidad.](../accessibility/accessibility.md)

 

 
