---
description: En este tema se describe cómo trabajar con perfiles ASF en Microsoft Media Foundation.
ms.assetid: 03a0981b-29c3-450d-aa58-bc56a76e6cb6
title: Perfil ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 616670e7de68fd73c168c474544fc6236f1586e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539646"
---
# <a name="asf-profile"></a>Perfil ASF

En este tema se describe cómo trabajar con perfiles ASF en Microsoft Media Foundation.

Un archivo de formato de sistema avanzado (ASF) contiene una o más secuencias. Para cada flujo, el encabezado ASF contiene un encabezado de propiedades de secuencia que describe la secuencia. En el nivel [WMContainer](wmcontainer-asf-components.md) , se usan los siguientes objetos para establecer o leer las propiedades de las secuencias ASF:

-   Objeto de *perfil ASF* : describe las secuencias y sus relaciones entre sí. El objeto de perfil ASF expone la interfaz [**IMFASFProfile**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfprofile) .
-   Objeto de *configuración de secuencia* : describe una secuencia. El objeto de configuración de secuencia contiene un tipo de medio que describe el formato de la secuencia. En el caso de las secuencias de audio y vídeo, el tipo de archivo multimedia describe exactamente cómo se configura el flujo y lo usan los códecs que codifican o descodifican la secuencia. El objeto de configuración de secuencia expone la interfaz [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) . Un perfil ASF válido contiene al menos un objeto de configuración de la secuencia.
-   Objeto de *exclusión mutua* : describe varias secuencias que no se van a leer simultáneamente. Un objeto de exclusión mutua expone la interfaz [**IMFASFMutualExclusion**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfmutualexclusion) . Un perfil ASF contiene cero o más objetos de exclusión mutua.

En el diagrama siguiente se muestra la relación entre el perfil ASF y los objetos contenidos en el perfil.

![diagrama de árbol de un nodo de perfil ASF con nodos secundarios de configuración de secuencia; los primeros apuntan al tipo de medio, los dos siguientes a la exclusión mutua](images/asf-components02.png)

Para la reproducción, el perfil ASF se usa para enumerar las secuencias y buscar los formatos de flujo. Para la codificación, el perfil ASF se usa para configurar las secuencias en el archivo de destino.

El perfil ASF también se utiliza para configurar el [receptor de medios ASF](asf-media-sinks.md). Para cada flujo en el perfil ASF, el receptor de medios ASF crea un receptor de flujo correspondiente.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                           | Descripción                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [Creación de un perfil ASF](creating-an-asf-profile.md)<br/>                               | Describe cómo crear un objeto de perfil ASF.<br/>          |
| [Crear y configurar secuencias ASF](creating-and-configuring-asf-streams.md)<br/>     | Describe cómo agregar secuencias a un perfil ASF.<br/>         |
| [Usar exclusión mutua para secuencias ASF](using-mutual-exclusion-for-asf-streams.md)<br/> | Describe cómo agregar exclusiones mutuas a secuencias ASF. <br/> |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tipos de medios](media-types.md)
</dt> <dt>

[Tutorial: 1-pasar la codificación de Windows Media](tutorial--1-pass-windows-media-encoding.md)
</dt> <dt>

[Tutorial: escribir un archivo WMA con codificación CBR](tutorial--writing-a-wma-file-by-using-cbr-encoding.md)
</dt> <dt>

[Componentes de WMContainer ASF](wmcontainer-asf-components.md)
</dt> </dl>

 

 




