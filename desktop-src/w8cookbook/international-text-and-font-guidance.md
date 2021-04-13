---
title: Guía de texto y fuentes internacionales
description: Guía de texto y fuentes internacionales
ms.assetid: 0540C9AD-8774-4F0F-B013-48C3EAE59BF2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2f9d94c53e4db45666d28a7c23a0e883043ba27
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104420732"
---
# <a name="international-text-and-font-guidance"></a>Guía de texto y fuentes internacionales

## <a name="affected-platforms"></a>Plataformas afectadas

<dl> Clientes: Windows 8 \| Windows 8.1  
Servidores: Windows Server 2012 \| Windows server 2012 R2  
</dl>

## <a name="description"></a>Descripción

Como antes de Windows 2000, se ha agregado compatibilidad con la presentación de texto para nuevos scripts en cada versión principal de Windows. Puede encontrar descripciones de los cambios realizados en cada versión principal en el artículo [compatibilidad con fuentes y scripts para Windows](https://msdn.microsoft.com/goglobal/bb688099.aspx) en el [centro de desarrollo de go global](https://msdn.microsoft.com/goglobal/default).

Tenga en cuenta que la compatibilidad con un script puede requerir ciertos cambios en los componentes de la pila de texto, así como los cambios en las fuentes. El sistema operativo Windows tiene muchos componentes de pila de texto: DirectWrite, GDI, Uniscribe, GDI+, WPF, RichEdit, ComCtl32 y otros. La información proporcionada pertenece principalmente a GDI y a DirectWrite. También se aplica a los marcos de interfaz de usuario, como RichEdit o el agente de representación de MSHTML, que se usan para las aplicaciones de la tienda de Windows 8 y para representar el contenido Web, aunque dichos componentes pueden presentar ciertas diferencias.

## <a name="best-practices"></a>Prácticas recomendadas

**Orientación tipográfica para desarrolladores**

La tipografía está en el corazón del lenguaje de diseño de Microsoft. Cada uno de los principios de diseño de Microsoft refuerza la importancia de la tipografía. Por primera vez, los desarrolladores de aplicaciones tienen un conjunto de marcos que admiten características tipográficas avanzadas. Vaya a [Mostrar y editar texto](/previous-versions/windows/apps/hh465442(v=win.10)) para obtener información sobre cómo usar JavaScript y HTML para mostrar y editar texto en aplicaciones de la tienda Windows.

**Métricas de fuentes**

Las métricas de fuente son un área de importancia especial para los desarrolladores de aplicaciones. Los archivos de fuente contienen varios valores relacionados con las métricas verticales y horizontales. Estos valores están documentados en la [especificación OpenType](https://www.microsoft.com/typography/otspec/) y se exponen a través de una variedad de API que se encuentran en la [estructura de \_ \_ métricas de fuentes DWRITE](/windows/win32/api/dwrite/ns-dwrite-dwrite_font_metrics) y en la [estructura TEXTMETRIC](/windows/win32/api/wingdi/ns-wingdi-textmetrica).

## <a name="resources"></a>Recursos

-   [Compatibilidad con scripts y fuentes para Windows](https://msdn.microsoft.com/goglobal/bb688099.aspx)
-   [Vaya al centro de desarrollo global](https://msdn.microsoft.com/goglobal/default)
-   [Mostrar y editar texto](/previous-versions/windows/apps/hh465442(v=win.10))
-   [Especificación OpenType](https://www.microsoft.com/typography/otspec/)
-   [DWRITE \_ estructura de las \_ métricas de fuente](/windows/win32/api/dwrite/ns-dwrite-dwrite_font_metrics)
-   [Estructura TEXTMETRIC](/windows/win32/api/wingdi/ns-wingdi-textmetrica)

 

 