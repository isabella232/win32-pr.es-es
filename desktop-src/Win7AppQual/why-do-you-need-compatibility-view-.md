---
description: ¿Por qué necesita Vista de compatibilidad?
ms.assetid: 5B8D3A76-F30B-4F17-9257-0B6ED7F2D753
title: ¿Por qué necesita Vista de compatibilidad?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9991e9dc0c2edcd66ae6655c094f17b240be985a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108113383"
---
# <a name="why-do-you-need-compatibility-view"></a>¿Por qué necesita Vista de compatibilidad?

La Vista de compatibilidad sigue un conjunto de reglas para mostrar el contenido correctamente, sin necesidad de ninguna acción de usuario (o administrador de TI) siempre que sea posible. Vista de compatibilidad permite a los desarrolladores indicar al explorador qué motor de representación usar y permite a los usuarios invalidar los modos de elección y cambio del explorador. Si el desarrollador y el profesional de IT no especifican qué modo de representación usar, el usuario ve el icono de "página rota" en el extremo derecho de la barra de direcciones, como se muestra en la ilustración siguiente.

![ilustración del icono de página rota junto a la barra de direcciones](images/iecompatview.png)

Si un usuario hace clic en el icono, Windows Internet Explorer 8 cambia los modos de representación y la página se vuelve a cargar al instante.

Los usuarios no siempre ven este icono. Es una solución secundaria en lugar del mecanismo de compatibilidad de aplicaciones principal. Windows Internet Explorer muestra este icono solo cuando un cambio en Vista de compatibilidad tiene sentido, como cuando un usuario ve páginas en modo estándar. En todos los demás casos, como cuando un usuario ve páginas en modo o vistas sitios de zona de intranet, el icono no aparece. Para obtener más información sobre Vista de compatibilidad y cuándo aparece el icono, vea [Introducing Vista de compatibilidad](/archive/blogs/ie/).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Corrección de problemas de compatibilidad en aplicaciones web mediante Vista de compatibilidad](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 
