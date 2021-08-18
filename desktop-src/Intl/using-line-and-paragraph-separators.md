---
description: Las aplicaciones deben usar el carácter separador de líneas (0x2028) y el carácter separador de párrafos (0x2029) para dividir el texto sin formato. Se inicia una nueva línea después de cada separador de línea. Se inicia un nuevo párrafo detrás de cada separador de párrafo.
ms.assetid: 086aca6c-8d1f-4e54-9e1c-642be50b303c
title: Usar separadores de líneas y párrafos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 857d7cae4dc7bd720ca94e9780bcb83588650b3df578cd0216e2424c1b28d5af
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119764635"
---
# <a name="using-line-and-paragraph-separators"></a>Usar separadores de líneas y párrafos

Las aplicaciones deben usar el carácter separador de líneas (0x2028) y el carácter separador de párrafos (0x2029) para dividir el texto sin formato. Se inicia una nueva línea después de cada separador de línea. Se inicia un nuevo párrafo detrás de cada separador de párrafo.

No es necesario iniciar la primera línea o párrafo de un archivo con estos caracteres, ni finalizar la última línea o párrafo con ellos. Esto indica que hay una línea o párrafo vacíos en esa ubicación.

La aplicación puede usar el separador de líneas para indicar un extremo incondicional de la línea. Sin embargo, los separadores de línea no se corresponden con los caracteres de avance de línea y retorno de carro independientes o una combinación de estos caracteres. Los separadores de línea se deben procesar por separado de los caracteres de avance de línea y retorno de carro.

La aplicación puede insertar un separador de párrafos entre párrafos de texto. El uso de este separador permite la creación de archivos de texto sin formato que se pueden formatear con anchos de línea diferentes en diferentes sistemas operativos. El sistema de destino puede hacer caso omiso de los separadores de línea y realizar saltos entre párrafos solo en los separadores de párrafo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar caracteres especiales en Unicode](using-special-characters-in-unicode.md)
</dt> </dl>

 

 



