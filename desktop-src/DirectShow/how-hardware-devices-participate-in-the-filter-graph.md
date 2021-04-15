---
description: Cómo participan los dispositivos de hardware en el gráfico de filtros
ms.assetid: 27e1c097-9bb4-4f9c-b9f9-0d4225c0d290
title: Cómo participan los dispositivos de hardware en el gráfico de filtros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68794bbc046e633e9a435b2628a20b8ea8aab174
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104494308"
---
# <a name="how-hardware-devices-participate-in-the-filter-graph"></a>Cómo participan los dispositivos de hardware en el gráfico de filtros

En este artículo se describe cómo interactúa DirectShow con el hardware de audio y vídeo.

**Filtros de contenedor**

Todos los filtros de DirectShow son componentes de software de modo usuario. Para que un dispositivo de hardware en modo kernel, como una tarjeta de captura de vídeo, se unan a un gráfico de filtros de DirectShow, el dispositivo se debe representar como un filtro de modo de usuario. Esta función se realiza mediante los filtros de "contenedor" especializados que se proporcionan con DirectShow. Estos filtros incluyen el filtro de [captura de audio](audio-capture.md) , el filtro de [captura VFW](vfw-capture-filter.md) , el filtro de [sintonizador de TV](tv-tuner-filter.md) , el filtro de audio de [TV](tv-audio-filter.md) y el filtro de [Cruz analógica de vídeo](analog-video-crossbar-filter.md) . DirectShow también proporciona un filtro denominado KsProxy, que puede representar cualquier tipo de dispositivo de streaming Modelo de controlador de Windows (WDM). Los proveedores de hardware pueden extender KsProxy para admitir la funcionalidad personalizada, proporcionando un *complemento KsProxy*, que es un objeto com agregado por KsProxy.

Los filtros de contenedor exponen las interfaces COM que representan las funciones del dispositivo. La aplicación usa estas interfaces para pasar información hacia y desde el filtro. El filtro convierte las llamadas al método COM en llamadas de controlador de dispositivo, pasa esa información al controlador en modo kernel y, a continuación, convierte el resultado de nuevo en la aplicación. Los filtros sintonizador de TV, audio de TV, Cruz de vídeo analógico y KsProxy admiten propiedades de controlador personalizadas a través de la interfaz [**IKsPropertySet**](ikspropertyset.md) . El filtro de captura VFW y el filtro de captura de audio no se pueden extender de esta manera.

En el caso de los desarrolladores de aplicaciones, los filtros de contenedor permiten a la aplicación controlar los dispositivos de la misma forma que controlan cualquier otro filtro de DirectShow. No se requiere ninguna programación especial; los detalles de la comunicación con el dispositivo de modo kernel se encapsulan dentro del filtro.

**Vídeo para dispositivos Windows**

El filtro de captura VFW admite tarjetas de captura de vídeo para Windows (VfW) anteriores. Cuando una tarjeta VfW está presente en el sistema de destino, se puede detectar y agregar al gráfico de filtros mediante el [enumerador de dispositivos del sistema](system-device-enumerator.md)DirectShow. Para obtener más información, consulte [enumeración de dispositivos y filtros](enumerating-devices-and-filters.md).

**Dispositivos de captura y mezcla de audio (tarjetas de sonido)**

Las tarjetas de sonido más recientes tienen conectores de entrada para los micrófonos y otros tipos de dispositivos. Normalmente, estas tarjetas también tienen capacidades de combinación incorporada para controlar el volumen, el agudo y el bajo de cada entrada individual. En DirectShow, el filtro de captura de audio encapsula las entradas y el mezclador de la tarjeta de sonido. Cada tarjeta de sonido se puede detectar con el enumerador de dispositivos del sistema. Para ver las tarjetas de sonido del sistema, ejecute GraphEdit y seleccione en la categoría orígenes de captura de audio. Cada filtro de esa categoría es una instancia independiente del filtro de captura de audio. (Consulte [uso de GraphEdit](using-graphedit.md)).

**Dispositivos WDM streaming**

Los descodificadores de hardware y las tarjetas de captura más recientes se ajustan a la Especificación Modelo de controlador de Windows (WDM). Estos dispositivos tienen una mayor funcionalidad que los dispositivos VfW. Las tarjetas de captura de vídeo WDM pueden admitir características que no están disponibles en VfW, incluida la enumeración de formatos de captura, el control de los parámetros de vídeo, como matiz y brillo, selección de entrada mediante programación y compatibilidad con sintonizador de TV.

Para admitir dispositivos de transmisión por secuencias WDM, DirectShow proporciona el filtro KsProxy (ksproxy.ax). KsProxy se ha denominado "filtro de cuchilla de ejército de Suiza" porque hace muchas cosas diferentes. El número de PIN en el filtro y el número de interfaces COM que expone el filtro dependen de las capacidades del controlador subyacente. KsProxy no aparece en el gráfico de filtros bajo el nombre "KsProxy". Siempre toma el nombre descriptivo del dispositivo, que se encuentra en el registro. Para ver los dispositivos WDM del sistema, ejecute GraphEdit y seleccione una de las categorías de transmisión por secuencias WDM. Incluso si solo tiene una tarjeta WDM en el sistema, esa tarjeta podría contener más de un dispositivo. Cada dispositivo se representa como un filtro independiente, y cada uno de estos filtros es realmente KsProxy.

Una aplicación utiliza el enumerador de dispositivos del sistema para buscar monikers de dispositivo WDM en el sistema. Se crea una instancia de KsProxy mediante una llamada a **BindToObject** en el moniker. Dado que KsProxy puede representar todos los tipos de dispositivos WDM, debe consultar el controlador para determinar qué propiedad permite establecer el controlador. Los conjuntos de propiedades son colecciones de estructuras de datos usadas por los controladores WDM y también por algunos filtros de modo de usuario, como descodificadores de software MPEG-2. KsProxy se configura para exponer las interfaces COM que corresponden a esos conjuntos de propiedades. KsProxy traduce las llamadas a métodos COM en conjuntos de propiedades y las envía al controlador. Los proveedores de hardware pueden extender KsProxy mediante el suministro de complementos, que son interfaces específicas del proveedor que exponen las capacidades especiales de un dispositivo. Todos estos detalles están ocultos de la aplicación. La aplicación controla el dispositivo por medio de KsProxy, de la misma forma que cualquier otro filtro de DirectShow.

**Streaming de kernel**

Los dispositivos WDM admiten el streaming de kernel, en el que los datos se transmiten por completo en modo kernel sin cambiar al modo de usuario. Cambiar entre el modo kernel y el modo de usuario es costoso. el streaming de kernel permite velocidades de bits altas sin sobrecargar la CPU del host. Los filtros basados en WDM pueden usar el streaming de kernel para pasar datos multimedia directamente de un dispositivo de hardware a otro, en la misma tarjeta o en una tarjeta diferente, sin copiar los datos en la memoria principal del sistema.

Desde el punto de vista de una aplicación, aparece como si los datos se mueven de un filtro de modo de usuario al siguiente. En realidad, los datos podrían no pasar nunca al modo de usuario, pero en su lugar podrían transmitirse directamente desde un dispositivo de modo kernel a otro hasta que se represente en la tarjeta gráfica de vídeo. Algunos escenarios, como la captura en un archivo, requieren que los datos pasen del modo kernel al modo de usuario en algún momento. Sin embargo, este modificador no requiere necesariamente que los datos se copien en una nueva ubicación en la memoria.

Por lo general, los desarrolladores de aplicaciones no necesitan preocuparse por los detalles de la transmisión por secuencias del kernel, excepto como información general. Vea el DDK de Microsoft para obtener información más detallada sobre WDM, streaming de kernel, KsProxy y temas relacionados.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[El gráfico de filtro y sus componentes](the-filter-graph-and-its-components.md)
</dt> </dl>

 

 



