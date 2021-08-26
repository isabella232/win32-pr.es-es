---
title: Trabajar con perfiles
description: Trabajar con perfiles
ms.assetid: e1e31632-0db7-47db-a992-f5db9d8824c1
keywords:
- Windows SDK de formato multimedia, perfiles
- Windows SDK de formato multimedia, interfaz IWMCodecInfo3
- profiles,about
- profiles,Windows SDK de formato multimedia
- profiles,IWMCodecInfo3
- IWMCodecInfo3,about
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68982a47b743aaa12397e937ad9bd213fbd7ac0a78b41087d01929c1d42bb622
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120055435"
---
# <a name="working-with-profiles"></a>Trabajar con perfiles

En esta sección se describe cómo diseñar, crear y modificar perfiles. Cada perfil describe las secuencias que formarán un archivo y sus relaciones entre sí. Un objeto de perfil contiene información de configuración de secuencias para cada secuencia, información de exclusión mutua para secuencias que no se pueden entregar simultáneamente, información de uso compartido de ancho de banda e información de priorización de secuencias.

El propósito principal de los perfiles es proporcionar información de configuración de secuencias al objeto de escritor. El escritor usa la información de un perfil para coordinar con los códecs el proceso de compresión de entradas. Al configurar una secuencia multimedia comprimida, se especifica el códec que se usa para comprimir los datos y la configuración que usa el códec. También puede crear perfiles para secuencias sin comprimir. Se admiten varios tipos de secuencias sin comprimir. Aunque no requieren un códec, estos tipos tienen sus propios requisitos para la configuración de secuencias. Para obtener más información, vea [Configuring Secuencias](configuring-streams.md) [and Using Uncompressed Audio and Video Secuencias](using-uncompressed-audio-and-video-streams.md).

La información de configuración de secuencias de una secuencia mediante uno de los códecs Windows Media debe obtenerse del códec mediante los métodos de la interfaz [**IWMCodecInfo3.**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo3) El procedimiento para usar formatos de secuencia es diferente para los códecs de vídeo que para los códecs de audio, pero en ambos casos debe empezar por obtener el formato del códec. Nunca debe intentar configurar manualmente una secuencia mediante uno de los códecs de Windows Media, ya que los pequeños errores del perfil pueden tener un efecto profundo en el archivo ASF.

Los pasos básicos para crear o modificar perfiles son:

1.  Cree un perfil vacío o cargue un perfil existente para editarlo.
2.  Configure cada una de las secuencias, si es necesario, en función de los datos de perfil admitidos recuperados del códec que se usarán para codificar la secuencia.
3.  Configure la exclusión mutua, si es necesario.
4.  Configure el uso compartido de ancho de banda, si es necesario.
5.  Establezca la prioridad de las secuencias del archivo, si es necesario.

En las secciones siguientes se explica el proceso de creación y edición de perfiles.



| Sección                                                        | Descripción                                                                                        |
|----------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [Diseño de perfiles](designing-profiles.md)                   | Describe cómo diseñar un perfil.                                                                 |
| [Crear perfiles](creating-profiles.md)                     | Describe cómo crear un perfil vacío.                                                          |
| [Configuración de Secuencias](configuring-streams.md)                 | Describe cómo configurar secuencias e incluirlas en un perfil.                                  |
| [Uso de la exclusión mutua](using-mutual-exclusion.md)           | Describe cómo crear objetos de exclusión mutua e incluirlos en un perfil.                    |
| [Uso compartido de ancho de banda](using-bandwidth-sharing.md)         | Describe cómo usar el uso compartido de ancho de banda en un perfil.                                               |
| [Uso de la priorización de secuencias](using-stream-prioritization.md) | Describe cómo usar la priorización de secuencias en un perfil.                                           |
| [Guardar perfiles](saving-profiles.md)                         | Describe cómo guardar los perfiles personalizados en un archivo.                                              |
| [Uso de perfiles del sistema](using-system-profiles.md)             | Describe cómo trabajar con perfiles del sistema para ahorrar tiempo y esfuerzo en la creación de perfiles.           |
| [Administración del tamaño del paquete](managing-packet-size.md)               | Describe cómo controlar el tamaño de los paquetes en los flujos de datos de archivos realizados mediante el perfil. |



 

**Nota** Los usuarios de versiones anteriores del SDK Windows Media Format pueden estar acostumbrados a usar perfiles del sistema sin modificaciones para crear sus archivos. El SDK Windows Media Format 9 o posterior no incluye ningún perfil de sistema nuevo que use los códecs de la serie Windows Media 9 o versiones posteriores. Esto se debe al creciente número de perfiles que se necesitan para cubrir las distintas características que ahora ofrecen los códecs. Todavía puede usar los perfiles del sistema de la versión 8 como punto de partida para los perfiles. Para obtener más información, [vea Using System Profiles](using-system-profiles.md). Para obtener información sobre el nuevo mecanismo para dirigir perfiles a dispositivos de entrega específicos, consulte [Trabajar con plantillas de conformidad de dispositivos.](working-with-device-conformance-templates.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Características del archivo ASF**](asf-file-features.md)
</dt> <dt>

[**Guía de programación**](programming-guide.md)
</dt> </dl>

 

 




