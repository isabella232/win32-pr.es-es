---
title: Trabajar con perfiles
description: Trabajar con perfiles
ms.assetid: e1e31632-0db7-47db-a992-f5db9d8824c1
keywords:
- Windows Media Format SDK, perfiles
- SDK de Windows Media Format, interfaz IWMCodecInfo3
- perfiles, acerca de
- perfiles, SDK de Windows Media Format
- perfiles, IWMCodecInfo3
- IWMCodecInfo3, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 664bbafd6c628588aa3b45b0a62a216db7bd7749
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104420265"
---
# <a name="working-with-profiles"></a>Trabajar con perfiles

En esta sección se describe cómo diseñar, crear y modificar perfiles. Cada perfil describe las secuencias que compondrán un archivo y sus relaciones entre sí. Un objeto de perfil contiene información de configuración de secuencia para cada flujo, información de exclusión mutua de secuencias que no se pueden entregar simultáneamente, información de uso compartido de ancho de banda e información de priorización de flujo.

El propósito principal de los perfiles es proporcionar información de configuración de la secuencia al objeto escritor. El escritor usa la información de un perfil para coordinar con los códecs el proceso de compresión de entradas. Cuando se configura una secuencia multimedia comprimida, se especifica el códec que se usa para comprimir los datos y la configuración que usa el códec. También puede crear perfiles para secuencias sin comprimir. Se admiten varios tipos de flujo sin comprimir. Aunque no requieren un códec, estos tipos tienen sus propios requisitos para la configuración de la secuencia. Para obtener más información, consulte [configuración de secuencias](configuring-streams.md) y uso de secuencias de [audio y vídeo sin comprimir](using-uncompressed-audio-and-video-streams.md).

Los métodos de la interfaz [**IWMCodecInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo3) deben obtener la información de configuración de la secuencia de una secuencia mediante uno de los códecs de Windows Media. El procedimiento para usar formatos de secuencia es diferente para los códecs de vídeo que para los códecs de audio, pero en ambos casos debe empezar por obtener el formato del códec. Nunca debe intentar configurar manualmente una secuencia mediante uno de los códecs de Windows Media, ya que los pequeños errores en el perfil pueden tener un efecto profundo en el archivo ASF.

Los pasos básicos para crear o modificar perfiles son:

1.  Cree un perfil vacío o cargue uno existente para editarlo.
2.  Configure cada una de las secuencias, si es necesario, en función de los datos de perfil admitidos recuperados del códec que se utilizará para codificar la secuencia.
3.  Configure la exclusión mutua, si es necesario.
4.  Configure el uso compartido del ancho de banda, si es necesario.
5.  Establezca la prioridad de las secuencias en el archivo, si es necesario.

En las secciones siguientes se explica el proceso de creación y edición de perfiles.



| Sección                                                        | Descripción                                                                                        |
|----------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [Diseñar perfiles](designing-profiles.md)                   | Describe cómo diseñar un perfil.                                                                 |
| [Crear perfiles](creating-profiles.md)                     | Describe cómo crear un perfil vacío.                                                          |
| [Configuración de secuencias](configuring-streams.md)                 | Describe cómo configurar secuencias e incluirlas en un perfil.                                  |
| [Usar exclusión mutua](using-mutual-exclusion.md)           | Describe cómo crear objetos de exclusión mutua e incluirlos en un perfil.                    |
| [Uso del uso compartido de ancho de banda](using-bandwidth-sharing.md)         | Describe cómo utilizar el uso compartido de ancho de banda en un perfil.                                               |
| [Usar la priorización de flujos](using-stream-prioritization.md) | Describe cómo usar la priorización de secuencias en un perfil.                                           |
| [Guardar perfiles](saving-profiles.md)                         | Describe cómo guardar los perfiles personalizados en un archivo.                                              |
| [Usar perfiles del sistema](using-system-profiles.md)             | Describe cómo trabajar con perfiles del sistema para ahorrar tiempo y esfuerzo en la creación de perfiles.           |
| [Administración del tamaño del paquete](managing-packet-size.md)               | Describe cómo controlar el tamaño de los paquetes en los flujos de datos de los archivos creados con el perfil. |



 

**Nota:** Los usuarios de versiones anteriores del SDK de Windows Media Format pueden estar acostumbrados a usar perfiles del sistema sin modificaciones para crear sus archivos. El SDK de Windows Media Format 9 series o posterior no incluye ningún perfil de sistema nuevo que use Windows Media 9 series o códecs posteriores. Esto se debe al creciente número de perfiles que serían necesarios para cubrir las distintas características que ahora ofrecen los códecs. Todavía puede usar los perfiles del sistema de la versión 8 como punto de partida para los perfiles. Para obtener más información, consulte [Using System profiles](using-system-profiles.md). Para obtener información sobre el nuevo mecanismo de destino de perfiles para dispositivos de entrega específicos, consulte [trabajar con plantillas](working-with-device-conformance-templates.md)de cumplimiento de dispositivos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Características de archivos ASF**](asf-file-features.md)
</dt> <dt>

[**Guía de programación**](programming-guide.md)
</dt> </dl>

 

 




