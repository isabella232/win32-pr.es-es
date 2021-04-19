---
description: .
ms.assetid: 5B8D3A76-F30B-4F17-9257-0B6ED7F2D753
title: ¿Por qué necesita la vista de compatibilidad?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74fd1902ad77af863e61be36800a8c4f9eabf227
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688584"
---
# <a name="why-do-you-need-compatibility-view"></a>¿Por qué necesita la vista de compatibilidad?

La característica vista de compatibilidad sigue un conjunto de reglas para mostrar el contenido correctamente, sin que se necesiten acciones de usuario (o administrador de TI) siempre que sea posible. La vista de compatibilidad permite a los desarrolladores indicar al explorador qué motor de representación usar y permite a los usuarios invalidar los modos de elección y cambio del explorador. Si el desarrollador y el profesional de ti no especifican el modo de representación que se va a usar, el usuario verá el icono de "página rota" en el extremo derecho de la barra de direcciones, tal como se muestra en la siguiente ilustración.

![Ilustración del icono de página rota junto a la barra de direcciones](images/iecompatview.png)

Si un usuario hace clic en el icono, Windows Internet Explorer 8 cambia los modos de representación y la página se recarga al instante.

Los usuarios no siempre ven este icono. Es una solución secundaria en lugar del mecanismo de compatibilidad de aplicaciones principal. Windows Internet Explorer muestra este icono solo cuando tiene sentido un cambio en la vista de compatibilidad, como cuando un usuario ve las páginas del modo estándar. En todos los demás casos, como cuando un usuario ve las páginas del modo no estándar o las vistas sitios de la zona de intranet, el icono no aparece. Para obtener más información acerca de la vista de compatibilidad y el momento en el que aparece el icono, vea Introducción a la [vista de compatibilidad](/archive/blogs/ie/).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Corregir problemas de compatibilidad en aplicaciones web mediante la vista de compatibilidad](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 
