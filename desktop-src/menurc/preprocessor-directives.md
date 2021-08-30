---
title: Directivas de preprocesador (menús y otros recursos)
description: Puede usar las directivas descritas en la tabla siguiente según sea necesario en el script de recursos. Indica a RC que realice acciones o asigne valores a los nombres.
ms.assetid: 162f946e-54d8-4e23-9aa7-8e91eda4ee68
keywords:
- compilador de recursos, directivas de preprocesador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cff779f74c43e1498136b9f1b9d4a6e90fbeb453b8fb7cb2f6cbe3489af74e95
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119847275"
---
# <a name="preprocessor-directives-menus-and-other-resources"></a>Directivas de preprocesador (menús y otros recursos)

Puede usar las directivas descritas en la tabla siguiente según sea necesario en el script de recursos. Indica a RC que realice acciones o asigne valores a los nombres.



| Directiva                     | Descripción                                                           |
|-------------------------------|-----------------------------------------------------------------------|
| [**\#Definir**](-define.md)   | Define un nombre especificado al asignarle un valor determinado.               |
| [**\#elif**](-elif.md)       | Marca una cláusula opcional de un bloque de compilación condicional.          |
| [**\#else**](-else.md)       | Marca la última cláusula opcional de un bloque de compilación condicional.    |
| [**\#endif**](-endif.md)     | Marca el final de un bloque de compilación condicional.                     |
| [**\#if**](-if.md)           | Compila condicionalmente el script si una expresión especificada es true.  |
| [**\#ifdef**](-ifdef.md)     | Compila condicionalmente el script si se define un nombre especificado.     |
| [**\#ifndef**](-ifndef.md)   | Compila condicionalmente el script si no se define un nombre especificado. |
| [**\#incluír**](-include.md) | Copia el contenido de un archivo en el archivo de definición de recursos.      |
| [**\#undef**](-undef.md)     | Quita la definición del nombre especificado.                         |



 

Para definir símbolos para los identificadores de recursos, use la **\# directiva define** para definirlos en un archivo de encabezado. Incluya este encabezado tanto en el script de recursos como en el código fuente de la aplicación. De forma similar, los valores de los atributos y estilos de recursos se definen incluyendo Windows.h en el script de recursos.

RC trata los archivos con las extensiones .c y .h de una manera especial. Se supone que un archivo con una de estas extensiones no contiene recursos. Si un archivo tiene la extensión de nombre de archivo .c o .h, RC omite todas las líneas del archivo excepto las directivas de preprocesador. Por lo tanto, para incluir un archivo que contiene recursos en otro script de recursos, dé al archivo que se va a incluir una extensión que no sea .c o .h.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Directivas pragma](pragma-directives.md)
</dt> </dl>

 

 




