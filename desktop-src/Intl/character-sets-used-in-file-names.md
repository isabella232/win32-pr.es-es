---
description: NTFS almacena los nombres de archivo en Unicode. En cambio, los sistemas de archivos FAT12, FAT16 y FAT32 antiguos utilizan el juego de caracteres OEM. Para obtener más información, vea Páginas de códigos.
ms.assetid: 4573dd3b-ad68-460c-bc0f-ff65d4b70860
title: Juegos de caracteres usados en nombres de archivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79394c92b2886f715299855aae27f15753dc86cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910722"
---
# <a name="character-sets-used-in-file-names"></a>Juegos de caracteres usados en nombres de archivo

NTFS almacena los nombres de archivo en Unicode. En cambio, los sistemas de archivos FAT12, FAT16 y FAT32 antiguos utilizan el juego de caracteres OEM. Para obtener más información, vea [Páginas de códigos](code-pages.md).

A veces, las aplicaciones no Unicode que crean archivos FAT tienen que usar las funciones de conversión de la biblioteca en tiempo de ejecución estándar de C para traducir entre el juego de caracteres de la página de códigos de Windows y el juego de caracteres de página de códigos OEM. Con las implementaciones Unicode de las funciones del sistema de archivos, no es necesario realizar dichas traducciones.

La aplicación puede usar tipos de cadena genéricos, como se describe en [tipos de datos de Windows para cadenas](windows-data-types-for-strings.md). La aplicación también puede utilizar prototipos de función genéricos mediante técnicas descritas en [convenciones para prototipos de función](conventions-for-function-prototypes.md). En el caso de tipos de cadena genéricos o prototipos de función genéricos, la aplicación puede usar un solo archivo de código fuente para compilar una versión de Unicode o no Unicode. Para ello, la aplicación proporciona macros para las funciones que no se invocan al compilar para Unicode.

En los sistemas de archivos NTFS y FAT, los caracteres de nombre de archivo especiales son: ' \\ ', '/', '. ', '? ' y ' \* '. En las páginas de códigos OEM, estos caracteres especiales están en el intervalo ASCII de caracteres (de 0x00 a 0x7F). Sus equivalentes de Unicode son los mismos valores en un formato de 2 bytes, 0x0000 a 0x007F.

> [!Caution]  
> Los juegos de caracteres de página de códigos de Windows y de página de códigos OEM utilizados en los sistemas operativos en idioma japonés contienen el símbolo del yen (¥) en lugar de una barra diagonal inversa ( \\ ). Por lo tanto, el símbolo del yen es un carácter prohibido para los sistemas de archivos NTFS y FAT. Al asignar Unicode a una página de códigos en idioma japonés, [**WideCharToMultiByte**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte) y otras funciones de conversión asignan la barra diagonal inversa (u + 005C) y el símbolo de yen Unicode normal (u + 00A5) a este mismo carácter. Por motivos de seguridad, las aplicaciones no suelen permitir el carácter U + 00A5 en una cadena Unicode que podría convertirse para su uso como nombre de archivo FAT. Para obtener más información, vea [consideraciones de seguridad: características internacionales](security-considerations--international-features.md).

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Unicode en la API de Windows](unicode-in-the-windows-api.md)
</dt> <dt>

[Consideraciones de seguridad: características internacionales](security-considerations--international-features.md)
</dt> </dl>

 

 



