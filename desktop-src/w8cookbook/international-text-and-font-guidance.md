---
title: Guía internacional de texto y fuente
description: Guía internacional de texto y fuente
ms.assetid: 0540C9AD-8774-4F0F-B013-48C3EAE59BF2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2f9d94c53e4db45666d28a7c23a0e883043ba27
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127362847"
---
# <a name="international-text-and-font-guidance"></a>Guía internacional de texto y fuente

## <a name="affected-platforms"></a>Plataformas afectadas

<dl> Clientes: Windows 8 \| Windows 8.1  
Servidores: Windows Server 2012 \| Windows Server 2012 R2  
</dl>

## <a name="description"></a>Descripción

Desde antes Windows 2000, se ha agregado compatibilidad con la visualización de texto para nuevos scripts en cada versión principal de Windows. Puede encontrar descripciones de los cambios realizados en cada versión principal en el artículo Compatibilidad con scripts y fuentes [para](https://msdn.microsoft.com/goglobal/bb688099.aspx) Windows en el Centro de desarrollo [global de Go](https://msdn.microsoft.com/goglobal/default).

Tenga en cuenta que la compatibilidad con un script puede requerir ciertos cambios en los componentes de la pila de texto, así como cambios en las fuentes. El Windows operativo tiene muchos componentes de pila de texto: DirectWrite, GDI, Uniscribe, GDI+, WPF, RichEdit, ComCtl32 y otros. La información proporcionada pertenece principalmente a GDI y DirectWrite. También se suele aplicar a marcos de interfaz de usuario como RichEdit o el agente de representación MSHTML que se usa para aplicaciones de Windows 8 Store y para representar contenido web, aunque esos componentes pueden presentar ciertas diferencias.

## <a name="best-practices"></a>Prácticas recomendadas

**Guía de tipografía para desarrolladores**

La tipografía es el núcleo del lenguaje de diseño de Microsoft. Cada uno de los principios de diseño de Microsoft refuerza la importancia de la tipografía. Por primera vez, los desarrolladores de aplicaciones tienen un conjunto de marcos que admiten características tipográficas avanzadas. Vaya a [Mostrar y editar texto](/previous-versions/windows/apps/hh465442(v=win.10)) para obtener información sobre cómo usar JavaScript y HTML para mostrar y editar texto en Windows Store.

**Métricas de fuente**

Las métricas de fuente son un área de especial importancia para los desarrolladores de aplicaciones. Los archivos de fuente contienen varios valores relacionados con las métricas verticales y horizontales. Estos valores se documentan en la especificación [OpenType](https://www.microsoft.com/typography/otspec/) y se exponen a través de una variedad de API que se encuentran en DWRITE FONT METRICS structure (Estructura DE [ \_ MÉTRICAS \_ ](/windows/win32/api/dwrite/ns-dwrite-dwrite_font_metrics) DE FUENTE DE DWRITE) y [en TEXTMETRIC Structure (Estructura TEXTMETRIC).](/windows/win32/api/wingdi/ns-wingdi-textmetrica)

## <a name="resources"></a>Recursos

-   [Compatibilidad con scripts y fuentes para Windows](https://msdn.microsoft.com/goglobal/bb688099.aspx)
-   [Centro de desarrollo global de Go](https://msdn.microsoft.com/goglobal/default)
-   [Visualización y edición de texto](/previous-versions/windows/apps/hh465442(v=win.10))
-   [Especificación openType](https://www.microsoft.com/typography/otspec/)
-   [Estructura DE \_ MÉTRICAS DE FUENTES \_ DWRITE](/windows/win32/api/dwrite/ns-dwrite-dwrite_font_metrics)
-   [TEXTMETRIC (estructura)](/windows/win32/api/wingdi/ns-wingdi-textmetrica)

 

 