---
title: Copia de seguridad en cinta
description: Un volumen de cinta consta de un medio de grabación y su operador físico. Cada volumen de cinta tiene una o varias particiones. Las particiones normalmente se dividen en secciones por marcas de archivo o marcas de conjunto. Hay tres tipos de marcas de archivo.
ms.assetid: 2057e6e4-b674-4151-b3b6-bde5d87d10c1
keywords:
- copia de seguridad de copia de seguridad, cinta
- copia de seguridad en cinta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 217c1a536b8a1a345218d3748c6207e9b336b84eca4cea0f4e48b4e84c521733
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119588835"
---
# <a name="tape-backup"></a>Copia de seguridad en cinta

Un *volumen de cinta* consta de un medio de grabación y su operador físico. La longitud completa de la cinta de un volumen no está disponible para grabar datos. Las secciones cortas al principio y al final de la cinta están reservadas para conectar la cinta a los concentradores del operador. La primera posición de la cinta en la que se pueden grabar los datos es la denominada marcador de principio de medio *y* la última posición se denomina marcador de final *de medio.*

Cada volumen de cinta tiene una o varias particiones. Una partición es una parte del volumen, que contiene sus propios puntos inicial y final, que no se superpone con ninguna otra parte del volumen. Cada partición tiene tres posiciones predefinidas. La primera posición de una partición en la que se pueden registrar datos se denomina marcador de principio de partición y la última se denomina marcador de fin de *partición*. El *marcador de advertencia temprana* se encuentra inmediatamente antes del marcador de fin de partición. La posición de advertencia temprana notifica a las aplicaciones de cinta que transfieran datos almacenados en búfer a la cinta antes de llegar al marcador de fin de partición.

El área entre los puntos inicial y final de una partición normalmente se divide en secciones mediante marcas de *archivo* o marcas *de conjunto.* Las marcas de archivo y las marcas de conjunto son elementos especiales registrados que no contienen datos de usuario; simplemente dividen la partición en áreas más pequeñas para proporcionar un esquema de direcciones. Las marcas de archivo y las marcas de conjunto sirven para propósitos similares, pero las marcas de conjunto proporcionan un posicionamiento más rápido en unidades de cinta de alta capacidad.

Normalmente, los dispositivos de cinta admiten marcas de archivo y marcas de conjunto. La compatibilidad de ambos permite dar formato a los datos de cinta de forma que establezca marcas de datos independientes de diferentes volúmenes de disco y marcas de archivo independientes de los archivos individuales de un volumen de disco.

Otro elemento grabado que denota ubicaciones en la cinta es un espacio de *borrado,* un área de cinta borrada o un patrón que el dispositivo no reconoce como marca o como datos de usuario.

Hay tres tipos de marcas de archivo. Una *marca de archivo corta* contiene un espacio de borrado corto que no se puede sobrescribir a menos que la operación de escritura se realice desde el principio de la partición o desde una marca de archivo larga anterior. Una *marca de archivo larga* contiene un intervalo de borrado largo que permite a una aplicación colocar la cinta al principio de la marca de archivo y sobrescribir la marca de archivo y la brecha de borrado. Una *marca de archivo normal* no contiene un intervalo de borrado. Los dispositivos de cinta que usan marcas de archivo admiten marcas de archivo cortas y largas o marcas de archivo normales, pero no las tres.

El área de una partición entre marcas de conjunto o marcas de archivo está disponible para registrar datos. Una unidad de datos escritos en una cinta o leídos desde esta se conoce como bloque.

Para obtener más información, vea los temas siguientes:

-   [Inicialización de cintas](tape-initialization.md)
-   [Entrada y salida de cinta](tape-input-and-output.md)
-   [Creación de una aplicación de copia de seguridad](creating-a-backup-application.md)
-   [Copia de seguridad y restauración de vínculos duros](backing-up-and-restoring-hard-links.md)

 

 




