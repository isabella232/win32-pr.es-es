---
description: NTFS almacena nombres de archivo en Unicode. Por el contrario, los sistemas de archivos FAT12, FAT16 y FAT32 más antiguos usan el juego de caracteres OEM. Para obtener más información, vea Páginas de códigos.
ms.assetid: 4573dd3b-ad68-460c-bc0f-ff65d4b70860
title: Juegos de caracteres usados en nombres de archivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2dad9033b3ea723de757c59a73fc62c91a56da286ca74ca7444f31db42ff539f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120107385"
---
# <a name="character-sets-used-in-file-names"></a>Juegos de caracteres usados en nombres de archivo

NTFS almacena nombres de archivo en Unicode. Por el contrario, los sistemas de archivos FAT12, FAT16 y FAT32 más antiguos usan el juego de caracteres OEM. Para obtener más información, vea [Páginas de códigos](code-pages.md).

Las aplicaciones que no son Unicode que crean archivos FAT a veces tienen que usar las funciones de conversión de biblioteca en tiempo de ejecución de C estándar para traducir entre el juego de caracteres de página de códigos de Windows y el juego de caracteres de página de códigos oem. Con las implementaciones Unicode de las funciones del sistema de archivos, no es necesario realizar estas traducciones.

La aplicación puede usar tipos de cadena genéricos, como se describe [Windows tipos de datos para cadenas](windows-data-types-for-strings.md). La aplicación también puede usar prototipos de función genéricos mediante las técnicas descritas en [Convenciones para prototipos de función](conventions-for-function-prototypes.md). Para los tipos de cadena genéricos o los prototipos de función genéricos, la aplicación puede usar un único archivo de código fuente para compilar una versión Unicode o no Unicode. Para permitir esto, la aplicación proporciona macros para las funciones que no se invocan al compilar para Unicode.

En los sistemas de archivos NTFS y FAT, los caracteres de nombre de archivo especiales son: \\ ', '/', '.', '?' y ' \* '. En las páginas de códigos oem, estos caracteres especiales están en el intervalo ASCII de caracteres (0x00 a 0x7F). Sus equivalentes Unicode son los mismos valores en un formato de 2 bytes, 0x0000 a 0x007F.

> [!Caution]  
> Windows la página de códigos y los juegos de caracteres de página de códigos OEM usados en sistemas operativos en japonés contienen el símbolo Yen ():) en lugar de una barra diagonal inversa ( \\ ). Por lo tanto, el símbolo Yen es un carácter prohibido para los sistemas de archivos NTFS y FAT. Al asignar Unicode a una página de códigos en japonés, [**WideCharToMultiByte**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte) y otras funciones de conversión asignan la barra diagonal inversa (U+005C) y el símbolo Yen Unicode normal (U+00A5) a este mismo carácter. Por motivos de seguridad, las aplicaciones no deberían permitir normalmente el carácter U+00A5 en una cadena Unicode que podría convertirse para su uso como nombre de archivo FAT. Para obtener más información, vea [Security Considerations: International Features](security-considerations--international-features.md).

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Unicode en la API de Windows](unicode-in-the-windows-api.md)
</dt> <dt>

[Consideraciones de seguridad: Características internacionales](security-considerations--international-features.md)
</dt> </dl>

 

 



