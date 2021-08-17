---
description: El objetivo del reconocimiento del sistema de archivos es permitir que el sistema operativo Windows tenga una opción adicional para un sistema de archivos válido pero desconocido que no sea &\# 0034; Raw&\# 0034;.
ms.assetid: a5b1e97c-f22a-4d90-a3f4-1589ad9d1cc3
title: Reconocimiento del sistema de archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15cf33e8a6e3378ad5b9f0123cb78fa228b5b780e7440a2981b10982e76d187a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117996962"
---
# <a name="file-system-recognition"></a>Reconocimiento del sistema de archivos

El objetivo del reconocimiento del sistema de archivos es permitir que el sistema operativo Windows tenga una opción adicional para un sistema de archivos válido pero desconocido que no sea "RAW". Para ello, a partir de Windows 7 y Windows Server 2008 R2, el sistema define un tipo de estructura de datos fijo que se puede escribir en los medios en los que está activa una tecnología habilitada que modifica el formato del sistema de archivos. Esta estructura de datos, si está presente en el sector de disco lógico cero, sería reconocida por el sistema operativo y notificaría al usuario que el medio contiene un sistema de archivos válido pero desconocido y no es un volumen RAW si los controladores del sistema de archivos no están instalados.

## <a name="file-system-recognition-features-and-use"></a>Características y uso del reconocimiento del sistema de archivos

Varias tecnologías de almacenamiento recientes han modificado el formato del sistema de archivos en disco de forma que los medios en los que están habilitadas estas tecnologías se vuelven irreconocibles para las versiones anteriores de Windows debido a que los controladores del sistema de archivos no existen cuando se publicó una versión anterior determinada de Windows. El comportamiento predeterminado anterior en este escenario era el siguiente. Cuando el medio de almacenamiento no es un sistema de archivos conocido, se identifica como RAW y, a continuación, se propaga al shell de Windows, donde Reproducción automática se solicita con la interfaz de usuario (UI) de formato. El reconocimiento del sistema de archivos puede resolver esto si los autores del nuevo sistema de archivos escriben correctamente la estructura de [**datos adecuada**](file-system-recognition-structure.md) en el disco.

El reconocimiento del sistema de archivos usa las siguientes características y capas dentro del sistema operativo para lograr sus objetivos:

-   Storage, donde una estructura de datos fija reside como una secuencia de bytes organizada internamente en una estructura predefinida denominada estructura de datos [**FILE \_ SYSTEM RECOGNITION \_ \_ STRUCTURE.**](file-system-recognition-structure.md) Es responsabilidad del desarrollador del sistema de archivos crear esta estructura en disco correctamente.
-   Reconocimiento del sistema de archivos en el nivel de aplicación, logrado mediante el uso del código de control de E/S del dispositivo [**FSCTL \_ QUERY FILE \_ SYSTEM \_ \_ RECOGNITION.**](/windows/win32/api/winioctl/ni-winioctl-fsctl_query_file_system_recognition) Para obtener un ejemplo de cómo usar este código de control, vea [Obtener información de reconocimiento del sistema de archivos](obtaining-file-system-recognition-information.md).
-   Código de validación de suma de comprobación, almacenado dentro de la estructura de datos [**ESTRUCTURA DE RECONOCIMIENTO DEL SISTEMA \_ \_ \_ DE**](file-system-recognition-structure.md) ARCHIVOS. Para obtener un ejemplo de cómo calcular esta suma de comprobación, vea [Calcular una suma de comprobación de reconocimiento del sistema de archivos](computing-a-file-system-recognition-checksum.md).
-   La interfaz de usuario de Windows Shell usa las características enumeradas anteriormente para proporcionar una reproducción automática más flexible y sólida y compatibilidad relacionada con sistemas de archivos no reconocidos, pero solo puede funcionar si la estructura de datos [**FILE \_ SYSTEM RECOGNITION \_ \_ STRUCTURE**](file-system-recognition-structure.md) existe en el sector de disco lógico cero. Los desarrolladores que implementan nuevos sistemas de archivos deben usar este sistema para asegurarse de que su sistema de archivos no se supone erróneamente que es de tipo "RAW".

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Calcular una suma de comprobación de reconocimiento del sistema de archivos](computing-a-file-system-recognition-checksum.md)
</dt> <dt>

[Obtener información de reconocimiento del sistema de archivos](obtaining-file-system-recognition-information.md)
</dt> <dt>

[Obtención de información de volumen](obtaining-volume-information.md)
</dt> </dl>

 

 
