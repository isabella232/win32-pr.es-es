---
title: Copia de seguridad en cinta
description: Un volumen de cinta consta de un medio de grabación y su operador físico. Cada volumen de cinta tiene una o más particiones. Las particiones se dividen normalmente en secciones por filemarks o setmarks. Hay tres tipos de filemarks.
ms.assetid: 2057e6e4-b674-4151-b3b6-bde5d87d10c1
keywords:
- copia de seguridad, cinta
- Copia de seguridad de cinta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2820e512646642046059cb151061e3f605d56cd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075264"
---
# <a name="tape-backup"></a>Copia de seguridad en cinta

Un *volumen de cinta* consta de un medio de grabación y su operador físico. La longitud completa de la cinta de un volumen no está disponible para grabar datos. Las secciones cortas al principio y al final de la cinta se reservan para conectar la cinta a los concentradores del operador. La primera posición en la cinta donde se pueden grabar los datos es el llamado el *marcador de inicio de medio* y la última posición se denomina el *marcador de fin de medio*.

Cada volumen de cinta tiene una o más particiones. Una partición es una parte del volumen que contiene sus propios puntos inicial y final, que no se superpone con ninguna otra parte del volumen. Cada partición tiene tres posiciones predefinidas. La primera posición de una partición en la que se pueden grabar datos se denomina el *marcador de inicio de la partición* y el último se denomina *marcador de final de partición*. El *marcador de advertencia temprana* se encuentra inmediatamente antes del marcador de fin de partición. La posición de advertencia temprana notifica a las aplicaciones de cinta que transfieran los datos almacenados en búfer a la cinta antes de llegar al marcador de final de partición.

El área entre los puntos inicial y final de una partición se divide normalmente en secciones por *filemarks* o *setmarks*. Filemarks y setmarks son elementos grabados especiales que no contienen datos de usuario. simplemente dividen la partición en áreas más pequeñas para proporcionar un esquema de direcciones. Filemarks y setmarks atienden propósitos similares, pero setmarks proporcionan un posicionamiento más rápido en unidades de cinta de alta capacidad.

Normalmente, los dispositivos de cinta admiten filemarks y setmarks. La compatibilidad de ambos permite dar formato a los datos de la cinta de modo que setmarks separe los datos de diferentes volúmenes de disco y filemarks separan los datos de los archivos individuales de un volumen de disco.

Otro elemento grabado que denota ubicaciones en la cinta es una brecha de *borrado*, un área de cinta borrada o un patrón que el dispositivo no reconoce como una marca o como datos de usuario.

Hay tres tipos de filemarks. Una marca de tiempo *corta* contiene un espacio de borrado corto que no se puede sobrescribir a menos que la operación de escritura se realice desde el principio de la partición o desde una marca de tiempo larga anterior. Una marca de *tiempo larga* contiene un espacio de borrado largo que permite a una aplicación colocar la cinta al principio de la marca de tiempo y sobrescribir la marca de tiempo y la brecha de borrado. Una marca de error *normal* no contiene una brecha de borrado. Los dispositivos de cinta que usan filemarks admiten los valores Short y Long filemarks o normal filemarks, pero no los tres.

El área de una partición entre setmarks o filemarks está disponible para grabar datos. Una unidad de datos que se escriben en una cinta o se leen de ella se denomina bloque.

Para obtener más información, vea los temas siguientes:

-   [Inicialización de cinta](tape-initialization.md)
-   [Entrada y salida de cinta](tape-input-and-output.md)
-   [Crear una aplicación de copia de seguridad](creating-a-backup-application.md)
-   [Copia de seguridad y restauración de vínculos físicos](backing-up-and-restoring-hard-links.md)

 

 




