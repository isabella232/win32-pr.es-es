---
title: Archivos de respuesta
description: Como alternativa a colocar todas las opciones en la línea de comandos, el compilador MIDL acepta archivos de respuesta que contienen modificadores y argumentos.
ms.assetid: 53ee9ad2-1ab4-421f-99c9-66186da4bd9d
keywords:
- MIDL del compilador MIDL, archivos de respuesta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddd949a3704b0669fd37c5629307a59df9742010
ms.sourcegitcommit: ad8bd914e19508a67af232d8d59c0e0ee9c3948b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/07/2019
ms.locfileid: "104419226"
---
# <a name="response-files"></a>Archivos de respuesta

Como alternativa a colocar todas las opciones en la línea de comandos, el compilador MIDL acepta archivos de respuesta que contienen modificadores y argumentos. Un archivo de respuesta es un archivo de texto que contiene una o más opciones de la línea de comandos del compilador de MIDL. A diferencia de la línea de comandos, un archivo de respuesta permite varias líneas de opciones y nombres de archivo. Esto puede resultar útil debido a las limitaciones del entorno de compilación o como una comodidad para el proceso de compilación. Puede especificar un archivo de respuesta MIDL como:

 **\@ nombre de archivo** MIDL

<dl> <dt>

<span id="filename"></span><span id="FILENAME"></span>*extensión*
</dt> <dd>

Especifica el nombre del archivo de respuesta. El nombre del archivo de respuesta debe seguir inmediatamente al carácter @ sin ningún espacio en blanco entre el carácter @ y el nombre del archivo de respuesta.

</dd> </dl>

Las opciones de un archivo de respuesta se interpretan como si estuvieran presentes en ese lugar en la línea de comandos de MIDL. Cada argumento de un archivo de respuesta debe comenzar y finalizar en la misma línea. No se puede utilizar el carácter de barra diagonal inversa ( \) para concatenar líneas.

MIDL admite argumentos de línea de comandos que incluyen uno o varios archivos de respuesta, combinados con otros modificadores de la línea de comandos:

**MIDL-Oicf @midl1.rsp -envwin32 @midl2.rsp ITF. idl**

El compilador MIDL no admite archivos de respuesta anidados.

 

 




