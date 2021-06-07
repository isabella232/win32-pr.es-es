---
title: Archivos de respuesta
description: Como alternativa a colocar todas las opciones en la línea de comandos, el compilador MIDL acepta archivos de respuesta que contienen modificadores y argumentos.
ms.assetid: 53ee9ad2-1ab4-421f-99c9-66186da4bd9d
keywords:
- MIDL del compilador MIDL, archivos de respuesta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c9b4d079e92dff3c25f8a38c6c73073a548ea91
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111387083"
---
# <a name="response-files"></a>Archivos de respuesta

Como alternativa a colocar todas las opciones en la línea de comandos, el compilador MIDL acepta archivos de respuesta que contienen modificadores y argumentos. Un archivo de respuesta es un archivo de texto que contiene una o varias opciones de línea de comandos del compilador MIDL. A diferencia de una línea de comandos, un archivo de respuesta permite varias líneas de opciones y nombres de archivo. Esto puede ser útil debido a las limitaciones del entorno de compilación o por comodidad para el proceso de compilación. Puede especificar un archivo de respuesta MIDL como:

**midl** **\@ filename**

<dl> <dt>

<span id="filename"></span><span id="FILENAME"></span>*Nombre*
</dt> <dd>

Especifica el nombre del archivo de respuesta. El nombre del archivo de respuesta debe seguir inmediatamente el carácter @ sin espacio en blanco entre el carácter @ y el nombre del archivo de respuesta.

</dd> </dl>

Las opciones de un archivo de respuesta se interpretan como si estuvieran presentes en ese lugar en la línea de comandos de MIDL. Cada argumento de un archivo de respuesta debe comenzar y terminar en la misma línea. No se puede usar el carácter de barra diagonal inversa ( \\ ) para concatenar líneas.

MIDL admite argumentos de línea de comandos que incluyen uno o varios archivos de respuesta, combinados con otros modificadores de línea de comandos:

**midl -Oicf @midl1.rsp -envwin32 @midl2.rsp itf.idl**

El compilador MIDL no admite archivos de respuesta anidados.

 

 




