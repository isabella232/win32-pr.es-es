---
description: Creación de topología avanzada
ms.assetid: 66aa07d8-6756-4d5b-9f0a-24b902da6fa2
title: Creación de topología avanzada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49d7f2bba412a698d688bc9d88e9935ed0988cc909931634633a0d75b88c2fae
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119664875"
---
# <a name="advanced-topology-building"></a>Creación de topología avanzada

En esta sección se describen algunas técnicas avanzadas para crear topologías. Puede usar estas técnicas si desea tener más control sobre las topologías que envía a la sesión multimedia.

Dado que estas técnicas están pensadas para escenarios que van más allá de la funcionalidad proporcionada por el cargador de topologías estándar, muchos de los detalles dependerán de los requisitos concretos de la aplicación. Por lo tanto, esta sección se organiza de forma flexible en torno a subtareas más pequeñas, en lugar de escenarios completos de un extremo a otro.

La aplicación de reproducción típica sigue estos pasos:

1.  La aplicación compila una topología parcial y la pone en cola en la sesión multimedia.
2.  La sesión multimedia invoca el cargador de topologías para resolver la topología.

Si desea ir más allá de las funcionalidades del cargador de topologías, hay tres enfoques generales:

-   Cree una topología completa. Al poner en cola la topología en la sesión multimedia, llame a [**MFMediaSession::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) con la marca MFSESSION \_ SETTOPOLOGY \_ NORESOLUTION. Esta marca impide que la sesión multimedia intente resolver la topología.

-   Invoque directamente el cargador de topologías para resolver la topología. A continuación, puede modificar la topología completa antes de hacer cola en la sesión multimedia.

-   Implemente un cargador de topologías personalizado. Con este enfoque, pone en cola una topología parcial, pero la sesión multimedia invoca el cargador personalizado en lugar de la implementación Media Foundation estándar. Una ventaja de este enfoque es que puede realizar la creación de topología personalizada dentro del entorno protegido. (En ese caso, sin embargo, el cargador de topologías debe ser un componente de confianza. Para obtener más información, vea [Ruta de acceso de medios protegidos).](protected-media-path.md)

Esta sección contiene los temas siguientes.



| Tema                                                                          | Descripción                                                                                                      |
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| [Cargadores de topología personalizados](custom-topology-loaders.md)                         | Cómo proporcionar una implementación personalizada de [**IMFTopoLoader**](/windows/desktop/api/mfidl/nn-mfidl-imftopoloader) para la sesión multimedia.          |
| [Enlazar nodos de salida a receptores multimedia](binding-output-nodes-to-media-sinks.md) | Cómo preparar los nodos de salida en una topología si usa el cargador de topologías fuera de la sesión multimedia. |
| [Agregar un descodificador a una topología](adding-a-decoder-to-a-topology.md)           | Cómo seleccionar manualmente un descodificador y agregarlo a una topología.                                                       |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Topologías](topologies.md)
</dt> </dl>

 

 



