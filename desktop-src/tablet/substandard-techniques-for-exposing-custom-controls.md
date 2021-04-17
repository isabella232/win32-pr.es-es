---
description: Descripción de las técnicas de subestándar para exponer controles personalizados.
ms.assetid: 107968c6-c3b3-462d-b488-96c69f2b3b14
title: Técnicas subestándars para exponer controles personalizados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1194614474596b55e0b1cf0530a07f9b3c411f6e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678189"
---
# <a name="substandard-techniques-for-exposing-custom-controls"></a>Técnicas subestándars para exponer controles personalizados

Si una aplicación no admite Microsoft Active Accessibility, puede que no sea totalmente accesible. Las técnicas siguientes presentan controles parcialmente compatibles:

-   Devuelve una cadena descriptiva cuando el control se consulta mediante el mensaje de \_ GETTEXT de WM. Por ejemplo, permitir un equivalente personalizado de un control de botón con la etiqueta "Imprimir" para que se devuelva la cadena "botón Imprimir". Esto identifica el tipo de control y la etiqueta. La misma cadena es adecuada para un botón con una etiqueta que no sea texto, como un gráfico de una impresora. Del mismo modo, permitir un control personalizado que se comporta como una casilla para devolver la cadena de título "marca de impresión habilitada".
-   Admitir el mensaje de GETDLGCODE de WM \_ , que identifica la entrada del teclado que se admite. Por ejemplo, permitir un equivalente personalizado de un control de edición para administrar WM \_ GETDLGCODE devolviendo DLGC \_ HASSETSEL si controla los mensajes para establecer la selección, DLGC \_ WANTARROWS si usa las teclas de dirección y DLGC \_ WANTCHARS para indicar que utiliza la entrada de caracteres.
    > [!Note]  
    > Solo los controles que tienen sus propios identificadores de ventana pueden responder a los \_ mensajes de GETDLGCODE GETTEXT y WM \_ .

     

Para evitar problemas de compatibilidad con las ayudas de accesibilidad, debe seguir Active Accessibility instrucciones detalladas al diseñar controles personalizados. Para obtener más información sobre cómo evitar problemas de compatibilidad con las ayudas de accesibilidad, consulte la sección [accesibilidad](../accessibility/accessibility.md) .

 

 
