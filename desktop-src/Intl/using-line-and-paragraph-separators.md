---
description: Las aplicaciones deben usar el carácter separador de línea (0x2028) y el carácter separador de párrafo (0x2029) para dividir el texto sin formato. Se inicia una nueva línea después de cada separador de línea. Se inicia un nuevo párrafo detrás de cada separador de párrafo.
ms.assetid: 086aca6c-8d1f-4e54-9e1c-642be50b303c
title: Usar separadores de línea y de párrafo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2c9511ba2a8889b3c9139daf1d088d91ed746db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279496"
---
# <a name="using-line-and-paragraph-separators"></a>Usar separadores de línea y de párrafo

Las aplicaciones deben usar el carácter separador de línea (0x2028) y el carácter separador de párrafo (0x2029) para dividir el texto sin formato. Se inicia una nueva línea después de cada separador de línea. Se inicia un nuevo párrafo detrás de cada separador de párrafo.

No es necesario iniciar la primera línea o párrafo de un archivo con estos caracteres o finalizar la última línea o párrafo. Si lo hace, indicará que hay una línea o un párrafo vacíos en esa ubicación.

La aplicación puede utilizar el separador de línea para indicar un final de línea incondicional. Sin embargo, los separadores de línea no se corresponden con los caracteres de avance de línea y retorno de carro independientes o una combinación de estos caracteres. Los separadores de línea se deben procesar por separado de los caracteres de avance de línea y retorno de carro.

La aplicación puede insertar un separador de párrafo entre párrafos de texto. El uso de este separador permite la creación de archivos de texto sin formato que se pueden formatear con anchos de línea diferentes en diferentes sistemas operativos. El sistema de destino puede hacer caso omiso de los separadores de línea y realizar saltos entre párrafos solo en los separadores de párrafo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar caracteres especiales en Unicode](using-special-characters-in-unicode.md)
</dt> </dl>

 

 



