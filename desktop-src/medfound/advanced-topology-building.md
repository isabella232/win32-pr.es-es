---
description: Creación de topologías avanzadas
ms.assetid: 66aa07d8-6756-4d5b-9f0a-24b902da6fa2
title: Creación de topologías avanzadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b4cc061d4e557dda4ccbb81eabc55e8e1b3e33b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360266"
---
# <a name="advanced-topology-building"></a>Creación de topologías avanzadas

En esta sección se describen algunas técnicas avanzadas para crear topologías. Puede usar estas técnicas si desea tener más control sobre las topologías que envía a la sesión multimedia.

Dado que estas técnicas están pensadas para escenarios que van más allá de la funcionalidad proporcionada por el cargador de topología estándar, muchos de los detalles dependerán de los requisitos específicos de la aplicación. Por lo tanto, esta sección está organizada de forma flexible en torno a subtareas más pequeñas, en lugar de escenarios completos.

La aplicación de reproducción típica sigue estos pasos:

1.  La aplicación crea una topología parcial y la pone en cola en la sesión multimedia.
2.  La sesión multimedia invoca el cargador de topología para resolver la topología.

Si desea ir más allá de las capacidades del cargador de topología, hay tres enfoques generales:

-   Cree una topología completa. Al poner en cola la topología en la sesión multimedia, llame a [**IMFMediaSession:: SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) con la \_ marca Resolution de MFSESSION SetTopology \_ . Esta marca impide que la sesión multimedia intente resolver la topología.

-   Invoque directamente el cargador de topología para resolver la topología. Después, puede modificar la topología completa antes de ponerla en cola en la sesión multimedia.

-   Implemente un cargador de topología personalizado. Con este enfoque, se pone en cola una topología parcial, pero la sesión multimedia invoca el cargador personalizado en lugar de la implementación de Media Foundation estándar. Una ventaja de este enfoque es que puede realizar la compilación de topología personalizada dentro del entorno protegido. En ese caso, sin embargo, el cargador de topología debe ser un componente de confianza. Para obtener más información, vea [ruta de acceso a medios protegidos](protected-media-path.md)).

Esta sección contiene los temas siguientes.



| Tema                                                                          | Descripción                                                                                                      |
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| [Cargadores de topología personalizados](custom-topology-loaders.md)                         | Cómo proporcionar una implementación personalizada de [**IMFTopoLoader**](/windows/desktop/api/mfidl/nn-mfidl-imftopoloader) para la sesión multimedia.          |
| [Enlazar nodos de salida a receptores de medios](binding-output-nodes-to-media-sinks.md) | Cómo preparar los nodos de salida en una topología si usa el cargador de topología fuera de la sesión de medios. |
| [Agregar un descodificador a una topología](adding-a-decoder-to-a-topology.md)           | Cómo seleccionar un descodificador manualmente y agregarlo a una topología.                                                       |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Topologías](topologies.md)
</dt> </dl>

 

 



