---
description: Atributos de topología
ms.assetid: 50102096-a29f-4c00-a685-179ba5d71089
title: Atributos de topología
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 286b6dbfe922461083b49d77ad2351e98d562d3b
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/10/2021
ms.locfileid: "105660101"
---
# <a name="topology-attributes"></a>Atributos de topología

Los siguientes atributos se aplican a las topologías.



| Atributo                                                                                                | Descripción                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [\_ \_ modo DXVA de topología \_ MF](mf-topology-dxva-mode.md)                                                    | Especifica si el cargador de topología habilita la aceleración de vídeo de Microsoft DirectX (DXVA) en la topología.                                                                                                                         |
| [\_cambio dinámico de topología MF \_ \_ \_ no \_ permitido](mf-topology-dynamic-change-not-allowed.md)                | Especifica si la sesión multimedia intenta modificar la topología cuando cambia el formato de una secuencia.                                                                                                                           |
| [\_topología MF \_ habilitar \_ XVP para la \_ \_ reproducción](mf-topology-enable-xvp-for-playback.md)                | Especifica si el cargador de topología habilita el procesador de vídeo de transcodificación (XVP). en el caso de las conversiones, habilitar la conversión de color acelerado de hardware.                                                                                        |
| [\_ \_ enumeración de los \_ tipos de origen \_ de la topología MF](mf-topology-enumerate-source-types.md)                         | Especifica si el cargador de topología enumera los tipos de medios proporcionados por el origen de medios.                                                                                                                                     |
| [modo de hardware de \_ topología MF \_ \_](mf-topology-hardware-mode.md)                                            | Especifica si se deben incluir las transformaciones basadas en hardware en la topología.                                                                                                                                                            |
| [**NO está en la \_ topología MF \_ \_ \_ MARKOUT**](mf-topology-no-markin-markout-attribute.md)                     | Especifica si la canalización recorta los ejemplos.                                                                                                                                                                                      |
| [velocidad de reproducción de \_ topología MF \_ \_](mf-topology-playback-framerate.md)                                  | Especifica la frecuencia de actualización del monitor.                                                                                                                                                                                                |
| [\_DiMS de reproducción de topologías \_ \_ máx \_ .](mf-topology-playback-max-dims.md)                                   | Especifica el tamaño de la ventana de destino para la reproducción de vídeo.                                                                                                                                                                   |
| [**\_PROJECTSTART de topología \_ MF**](mf-topology-projectstart-attribute.md)                                 | Especifica la hora de inicio de la topología dentro del segmento actual, en unidades de 100-nanosegundos.                                                                                                                                             |
| [**\_PROJECTSTOP de topología \_ MF**](mf-topology-projectstop-attribute.md)                                   | Especifica la hora de detención de la topología dentro del segmento actual, en unidades de 100-nanosegundos.                                                                                                                                              |
| [**Estado de resolución de \_ topología MF \_ \_**](mf-topology-resolution-status-attribute.md)                      | Especifica el estado de un intento de resolver una topología.                                                                                                                                                                          |
| [\_ \_ hora de inicio de la topología MF \_ \_ en el \_ conmutador de presentación \_](mf-topology-start-time-on-presentation-switch.md) | Especifica la hora de inicio de las presentaciones que se ponen en cola después de la primera presentación.                                                                                                                                           |
| [\_ \_ \_ optimizaciones de reproducción estática de topología MF \_](mf-topology-static-playback-optimizations.md)           | Habilita las optimizaciones estáticas en la canalización de vídeo.                                                                                                                                                                                |
| [\_Atributo de \_ desbloqueo FIELDOFUSE de MFT \_](mft-fieldofuse-unlock-attribute.md)                                | Contiene un puntero [**IMFFieldOfUseMFTUnlock**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) , que se usa para desbloquear una MFT con restricciones de campo de uso. Para obtener más información, consulte el [campo de restricciones de uso](field-of-use-restrictions.md). |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology)
</dt> <dt>

[Atributos de Media Foundation](media-foundation-attributes.md)
</dt> <dt>

[Atributos de nodo de topología](topology-node-attributes.md)
</dt> </dl>

 

 



