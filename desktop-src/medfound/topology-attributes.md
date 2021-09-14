---
description: Atributos de topología
ms.assetid: 50102096-a29f-4c00-a685-179ba5d71089
title: Atributos de topología
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 286b6dbfe922461083b49d77ad2351e98d562d3b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127268727"
---
# <a name="topology-attributes"></a>Atributos de topología

Los atributos siguientes se aplican a las topologías.



| Atributo                                                                                                | Descripción                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MODO \_ \_ DXVA DE TOPOLOGÍA \_ MF](mf-topology-dxva-mode.md)                                                    | Especifica si el cargador de topologías habilita la aceleración de vídeo de Microsoft DirectX (DXVA) en la topología.                                                                                                                         |
| [CAMBIO DINÁMICO DE TOPOLOGÍA DE MF \_ \_ NO \_ \_ \_ PERMITIDO](mf-topology-dynamic-change-not-allowed.md)                | Especifica si la sesión multimedia intenta modificar la topología cuando cambia el formato de una secuencia.                                                                                                                           |
| [TOPOLOGÍA \_ MF \_ HABILITACIÓN DE \_ XVP PARA LA \_ \_ REPRODUCCIÓN](mf-topology-enable-xvp-for-playback.md)                | Especifica si el cargador de topologías habilita el procesador de vídeo transcodificador (XVP). para conversiones, habilitando la conversión de color acelerada por hardware.                                                                                        |
| [TOPOLOGÍA \_ MF ENUMERA LOS TIPOS DE \_ \_ \_ ORIGEN](mf-topology-enumerate-source-types.md)                         | Especifica si el cargador de topología enumera los tipos de medios proporcionados por el origen de medios.                                                                                                                                     |
| [MODO \_ DE HARDWARE DE TOPOLOGÍA \_ \_ MF](mf-topology-hardware-mode.md)                                            | Especifica si se deben incluir transformaciones basadas en hardware en la topología.                                                                                                                                                            |
| [**TOPOLOGÍA \_ MF \_ SIN \_ MARKIN \_ MARKOUT**](mf-topology-no-markin-markout-attribute.md)                     | Especifica si la canalización recorta muestras.                                                                                                                                                                                      |
| [VELOCIDAD \_ DE FOTOGRAMAS DE \_ REPRODUCCIÓN DE \_ TOPOLOGÍA MF](mf-topology-playback-framerate.md)                                  | Especifica la frecuencia de actualización del monitor.                                                                                                                                                                                                |
| [ATENUACIONES \_ MÁXIMAS DE \_ REPRODUCCIÓN DE \_ TOPOLOGÍA \_ DE MF](mf-topology-playback-max-dims.md)                                   | Especifica el tamaño de la ventana de destino para la reproducción de vídeo.                                                                                                                                                                   |
| [**INICIO \_ DEL PROYECTO DE TOPOLOGÍA DE \_ MF**](mf-topology-projectstart-attribute.md)                                 | Especifica la hora de inicio de la topología dentro del segmento actual, en unidades de 100 nanosegundos.                                                                                                                                             |
| [**PROYECTOS \_ DE TOPOLOGÍA \_ MFTOP**](mf-topology-projectstop-attribute.md)                                   | Especifica el tiempo de detección de topología dentro del segmento actual, en unidades de 100 nanosegundos.                                                                                                                                              |
| [**ESTADO \_ DE RESOLUCIÓN DE TOPOLOGÍA DE \_ \_ MF**](mf-topology-resolution-status-attribute.md)                      | Especifica el estado de un intento de resolver una topología.                                                                                                                                                                          |
| [HORA \_ DE INICIO DE LA TOPOLOGÍA MF EN EL CONMUTADOR DE \_ \_ \_ \_ \_ PRESENTACIÓN](mf-topology-start-time-on-presentation-switch.md) | Especifica la hora de inicio de las presentaciones que se ponen en cola después de la primera presentación.                                                                                                                                           |
| [OPTIMIZACIONES \_ DE REPRODUCCIÓN ESTÁTICA DE TOPOLOGÍA \_ \_ \_ MF](mf-topology-static-playback-optimizations.md)           | Habilita las optimizaciones estáticas en la canalización de vídeo.                                                                                                                                                                                |
| [Atributo \_ MFT FIELDOFUSE \_ UNLOCK \_](mft-fieldofuse-unlock-attribute.md)                                | Contiene un [**puntero DE TIPO IMFFieldOfUseMFTUnlock,**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) que se usa para desbloquear un MFT con restricciones de campo de uso. Para obtener más información, [vea Restricciones de campo de uso.](field-of-use-restrictions.md) |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology)
</dt> <dt>

[Media Foundation atributos](media-foundation-attributes.md)
</dt> <dt>

[Atributos de nodo de topología](topology-node-attributes.md)
</dt> </dl>

 

 



