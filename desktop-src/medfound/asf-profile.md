---
description: En este tema se describe cómo trabajar con perfiles de ASF en Microsoft Media Foundation.
ms.assetid: 03a0981b-29c3-450d-aa58-bc56a76e6cb6
title: Perfil de ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 616670e7de68fd73c168c474544fc6236f1586e0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361187"
---
# <a name="asf-profile"></a>Perfil de ASF

En este tema se describe cómo trabajar con perfiles de ASF en Microsoft Media Foundation.

Un archivo de formato de sistemas avanzados (ASF) contiene una o varias secuencias. Para cada secuencia, el encabezado ASF contiene un encabezado de propiedades de flujo que describe la secuencia. En la [capa WMContainer,](wmcontainer-asf-components.md) se usan los siguientes objetos para establecer o leer las propiedades de los flujos de ASF:

-   Objeto de perfil de *ASF:* describe las secuencias y sus relaciones entre sí. El objeto de perfil ASF expone la [**interfaz DEFFProfile.**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfprofile)
-   *Objeto de configuración* de flujo: describe una secuencia. El objeto de configuración de flujo contiene un tipo de medio que describe el formato de la secuencia. En el caso de las secuencias de audio y vídeo, el tipo de medio describe exactamente cómo se configura la secuencia y la usan los códecs que codifican o descodifican la secuencia. El objeto de configuración de flujo expone la [**interfaz IMFASFStreamConfig.**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) Un perfil de ASF válido contiene al menos un objeto de configuración de flujo.
-   *Objeto de exclusión* mutua: describe varias secuencias que no están diseñadas para leerse simultáneamente. Un objeto de exclusión mutua expone la [**interfaz IMFASFMutualExclusion.**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfmutualexclusion) Un perfil de ASF contiene cero o más objetos de exclusión mutua.

En el diagrama siguiente se muestra la relación entre el perfil de ASF y los objetos contenidos en el perfil.

![diagrama de árbol de un nodo de perfil asf con nodos secundarios de configuración de flujo; el primero apunta al tipo de medio, los dos siguientes a la exclusión mutua](images/asf-components02.png)

Para la reproducción, el perfil de ASF se usa para enumerar las secuencias y buscar los formatos de secuencia. Para la codificación, el perfil de ASF se usa para configurar las secuencias en el archivo de destino.

El perfil de ASF también se usa para configurar el receptor [de medios de ASF.](asf-media-sinks.md) Para cada secuencia del perfil de ASF, el receptor de medios de ASF crea un receptor de flujo correspondiente.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                           | Descripción                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [Creación de un perfil de ASF](creating-an-asf-profile.md)<br/>                               | Describe cómo crear un objeto de perfil de ASF.<br/>          |
| [Creación y configuración de asf Secuencias](creating-and-configuring-asf-streams.md)<br/>     | Describe cómo agregar secuencias a un perfil de ASF.<br/>         |
| [Uso de la exclusión mutua para asf Secuencias](using-mutual-exclusion-for-asf-streams.md)<br/> | Describe cómo agregar exclusiones mutuas a los flujos de ASF. <br/> |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tipos de medios](media-types.md)
</dt> <dt>

[Tutorial: Codificación de medios de Windows paso 1](tutorial--1-pass-windows-media-encoding.md)
</dt> <dt>

[Tutorial: Escritura de un archivo WMA mediante la codificación CBR](tutorial--writing-a-wma-file-by-using-cbr-encoding.md)
</dt> <dt>

[Componentes de ASF de WMContainer](wmcontainer-asf-components.md)
</dt> </dl>

 

 




