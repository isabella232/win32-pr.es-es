---
description: Cómo participan los dispositivos de hardware en el filtro Graph
ms.assetid: 27e1c097-9bb4-4f9c-b9f9-0d4225c0d290
title: Cómo participan los dispositivos de hardware en el filtro Graph
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68794bbc046e633e9a435b2628a20b8ea8aab174
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127169918"
---
# <a name="how-hardware-devices-participate-in-the-filter-graph"></a>Cómo participan los dispositivos de hardware en el filtro Graph

En este artículo se describe DirectShow interactúa con el hardware de audio y vídeo.

**Filtros de contenedor**

Todos los DirectShow son componentes de software en modo de usuario. Para que un dispositivo de hardware en modo kernel, como una tarjeta de captura de vídeo, se una a un gráfico de filtros DirectShow, el dispositivo debe representarse como un filtro en modo de usuario. Esta función se realiza mediante filtros "contenedor" especializados proporcionados con DirectShow. Estos filtros incluyen el filtro de captura de [audio,](audio-capture.md) el filtro de captura [vfw,](vfw-capture-filter.md) el filtro de tv [tuner,](tv-tuner-filter.md) el filtro de [audio](tv-audio-filter.md) de tv y el filtro de barra cruzada [de vídeo](analog-video-crossbar-filter.md) análogo. DirectShow proporciona un filtro denominado KsProxy, que puede representar cualquier tipo de dispositivo de streaming Windows Driver Model (WDM). Los proveedores de hardware pueden extender KsProxy para admitir la funcionalidad personalizada, proporcionando un complemento *Ksproxy*, que es un objeto COM agregado por KsProxy.

Los filtros contenedor exponen interfaces COM que representan las funcionalidades del dispositivo. La aplicación usa estas interfaces para pasar información hacia y desde el filtro. El filtro convierte las llamadas del método COM en llamadas de controlador de dispositivo, pasa esa información al controlador en modo kernel y, a continuación, vuelve a traducir el resultado a la aplicación. Los filtros Tv Tuner, TV Audio, Analog Video Crossbar y KsProxy admiten propiedades de controlador personalizadas a través de la [**interfaz IKsPropertySet.**](ikspropertyset.md) El filtro de captura vfw y el filtro de captura de audio no son extensibles de esta manera.

Para los desarrolladores de aplicaciones, los filtros de contenedor permiten que la aplicación controle los dispositivos igual que cualquier otro filtro DirectShow aplicación. No se requiere ninguna programación especial; Los detalles de la comunicación con el dispositivo en modo kernel se encapsulan dentro del filtro.

**Vídeo para Windows dispositivos**

El filtro vfw capture admite las tarjetas de captura Video for Windows (VfW) anteriores. Cuando una tarjeta VfW está presente en el sistema de destino, se puede detectar y agregar al gráfico de filtros mediante el enumerador DirectShow del dispositivo [del sistema](system-device-enumerator.md). Para obtener más información, [consulte Enumeración de dispositivos y filtros.](enumerating-devices-and-filters.md)

**Dispositivos de captura y combinación de audio (tarjetas de sonido)**

Las tarjetas de sonido más recientes tienen conectores de entrada para micrófonos y otros tipos de dispositivos. Normalmente, estas tarjetas también tienen funcionalidades de combinación integradas para controlar el volumen, los triples y los sonidos de cada entrada individual. En DirectShow, las entradas y el mezclador de la tarjeta de sonido se encapsulan mediante el filtro de captura de audio. Cada tarjeta de sonido se puede detectar con el enumerador de dispositivos del sistema. Para ver las tarjetas de sonido en el sistema, ejecute GraphEdit y seleccione en la categoría Orígenes de captura de audio. Cada filtro de esa categoría es una instancia independiente del filtro de captura de audio. (Consulte [Uso de GraphEdit).](using-graphedit.md)

**Dispositivos de streaming WDM**

Los descodificadores de hardware y las tarjetas de captura más recientes se ajustan a la especificación Windows Driver Model (WDM). Estos dispositivos tienen una mayor funcionalidad que los dispositivos VfW. Las tarjetas de captura de vídeo WDM pueden admitir características que no están disponibles en VfW, incluida la enumeración de formatos de captura, el control mediante programación de parámetros de vídeo como el matiz y el brillo, la selección de entrada mediante programación y la compatibilidad con el ajuste de tv.

Para admitir dispositivos de streaming WDM, DirectShow proporciona el filtro KsProxy (ksproxy.ax). KsProxy se ha denominado "filtro de puñalada de campo de suiza" porque hace muchas cosas diferentes. El número de pines del filtro y el número de interfaces COM expuestas por el filtro dependen de las funciones del controlador subyacente. KsProxy no aparece en el gráfico de filtros con el nombre "KsProxy". Siempre toma el nombre descriptivo del dispositivo, que se encuentra en el registro. Para ver los dispositivos WDM en el sistema, ejecute GraphEdit y seleccione una de las categorías de WDM Streaming. Incluso si solo tiene una tarjeta WDM en el sistema, esa tarjeta puede contener más de un dispositivo. Cada dispositivo se representa como un filtro independiente y cada uno de estos filtros es en realidad KsProxy.

Una aplicación usa el enumerador de dispositivos del sistema para buscar monikers de dispositivo WDM en el sistema. Se crea una instancia de KsProxy mediante una **llamada a BindToObject** en el moniker. Dado que KsProxy puede representar todos los tipos de dispositivos WDM, debe consultar al controlador para determinar qué conjuntos de propiedades admite el controlador. Los conjuntos de propiedades son colecciones de estructuras de datos utilizadas por los controladores WDM y también por algunos filtros de modo de usuario, como descodificadores de software MPEG-2. KsProxy se configura para exponer las interfaces COM que corresponden a esos conjuntos de propiedades. KsProxy traduce las llamadas al método COM en conjuntos de propiedades y las envía al controlador. Los proveedores de hardware pueden extender KsProxy mediante el suministro de complementos, que son interfaces específicas del proveedor que exponen las funcionalidades especiales de un dispositivo. Todos estos detalles están ocultos en la aplicación. La aplicación controla el dispositivo mediante KsProxy, de la misma manera que cualquier otro DirectShow filtro.

**Kernel Streaming**

Los dispositivos WDM admiten el streaming de kernel, en el que los datos se transmiten completamente en modo kernel sin cambiar al modo de usuario. Cambiar entre el modo kernel y el modo de usuario es costoso desde el punto de vista computacional; El streaming de kernel permite velocidades de bits elevadas sin sobrecargar la CPU del host. Los filtros basados en WDM pueden usar el streaming de kernel para pasar datos multimedia directamente desde un dispositivo de hardware a otro, ya sea en la misma tarjeta o en otra tarjeta, sin copiar los datos en la memoria principal del sistema.

Desde el punto de vista de una aplicación, parece que los datos se mueven de un filtro de modo de usuario al siguiente. En realidad, es posible que los datos nunca pasen al modo de usuario en absoluto, sino que podrían transmitirse directamente desde un dispositivo en modo kernel a otro hasta que se representen en la tarjeta gráfica de vídeo. Algunos escenarios, como la captura en un archivo, requieren que los datos pasen del modo kernel al modo de usuario en algún momento. Sin embargo, este modificador no requiere necesariamente que los datos se copien en una nueva ubicación en memoria.

Por lo general, los desarrolladores de aplicaciones no necesitan preocuparse por los detalles del streaming del kernel, excepto como información general. Consulte Microsoft DDK para obtener información más detallada sobre WDM, streaming de kernel, KsProxy y temas relacionados.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[El filtro Graph y sus componentes](the-filter-graph-and-its-components.md)
</dt> </dl>

 

 



