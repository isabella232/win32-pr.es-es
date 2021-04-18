---
description: El objetivo del reconocimiento del sistema de archivos es permitir que el sistema operativo Windows tenga una opción adicional para un sistema de archivos válido pero no reconocido que no sea &\# 0034; RAW&\# 0034;.
ms.assetid: a5b1e97c-f22a-4d90-a3f4-1589ad9d1cc3
title: Reconocimiento del sistema de archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 457d4146588ba2db2b75d06c7afac10ecb18e87c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687274"
---
# <a name="file-system-recognition"></a>Reconocimiento del sistema de archivos

El objetivo del reconocimiento del sistema de archivos es permitir que el sistema operativo Windows tenga una opción adicional para un sistema de archivos válido pero no reconocido distinto de "sin procesar". Para lograr esto, a partir de Windows 7 y Windows Server 2008 R2, el sistema define un tipo de estructura de datos fijo que se puede escribir en el medio en el que está activa una tecnología habilitada que modifica el formato del sistema de archivos. Esta estructura de datos, si está presente en el sector cero del disco lógico, la reconocerá el sistema operativo y notificará al usuario que el medio contiene un sistema de archivos válido pero no reconocido y no es un volumen sin formato si los controladores del sistema de archivos no están instalados.

## <a name="file-system-recognition-features-and-use"></a>Características y uso de reconocimiento del sistema de archivos

Varias tecnologías de almacenamiento recientes han alterado el formato de sistema de archivos en disco de modo que el medio en el que están habilitadas estas tecnologías sea irreconocible en versiones anteriores de Windows debido a que los controladores del sistema de archivos no existen cuando se lanzó una versión anterior de Windows. El comportamiento predeterminado anterior en este escenario era el siguiente. Cuando el medio de almacenamiento no es un sistema de archivos conocido, se identifica como sin procesar y, a continuación, se propaga al shell de Windows, donde la reproducción automática solicita el formato de interfaz de usuario (UI). El reconocimiento del sistema de archivos puede solucionarlo si los autores del nuevo sistema de archivos escriben correctamente la [**estructura de datos**](file-system-recognition-structure.md) adecuada en el disco.

El reconocimiento del sistema de archivos usa las siguientes características y capas dentro del sistema operativo para lograr sus objetivos:

-   Medios de almacenamiento, donde una estructura de datos fija reside como una secuencia de bytes organizada internamente en una estructura predefinida denominada estructura de datos de la [**\_ \_ \_ estructura de reconocimiento del sistema de archivos**](file-system-recognition-structure.md) . Es responsabilidad del desarrollador del sistema de archivos crear esta estructura en disco correctamente.
-   Reconocimiento del sistema de archivos en el nivel de aplicación, conseguido mediante el uso del código de control de e/s del dispositivo de [**reconocimiento de sistema de archivos de consulta de FSCTL \_ \_ \_ \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_query_file_system_recognition) . Para obtener un ejemplo de cómo usar este código de control, vea [obtener información de reconocimiento del sistema de archivos](obtaining-file-system-recognition-information.md).
-   Código de validación de suma de comprobación, almacenado en la estructura de datos de la [**\_ \_ \_ estructura de reconocimiento del sistema de archivos**](file-system-recognition-structure.md) . Para obtener un ejemplo de cómo calcular esta suma de comprobación, consulte [calcular una suma de comprobación del reconocimiento del sistema de archivos](computing-a-file-system-recognition-checksum.md).
-   La interfaz de usuario del shell de Windows usa las características enumeradas anteriormente para proporcionar una reproducción automática más flexible y sólida y compatibilidad relacionada con los sistemas de archivos no reconocidos, pero solo puede funcionar si la estructura de datos de la [**\_ \_ \_ estructura de reconocimiento del sistema de archivos**](file-system-recognition-structure.md) existe en el sector del disco lógico cero. Los desarrolladores que implementan nuevos sistemas de archivos deben usar este sistema para asegurarse de que no se supone que el sistema de archivos es del tipo "sin procesar".

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Calcular una suma de comprobación del reconocimiento del sistema de archivos](computing-a-file-system-recognition-checksum.md)
</dt> <dt>

[Obtención de información de reconocimiento del sistema de archivos](obtaining-file-system-recognition-information.md)
</dt> <dt>

[Obtención de información de volumen](obtaining-volume-information.md)
</dt> </dl>

 

 
