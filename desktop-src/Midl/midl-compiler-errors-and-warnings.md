---
title: Errores y advertencias del compilador de MIDL
description: Al utilizar el compilador MIDL, los errores y las advertencias pueden deberse a un uso inadecuado de los modificadores de la línea de comandos o al contenido de los archivos IDL y ACF.
ms.assetid: 5c8d5a28-e559-4893-932f-b2306aefa932
keywords:
- Lenguaje de definición de interfaz de Microsoft MIDL, referencia
- MIDL del compilador MIDL, errores
- MIDL del compilador, errores
- errores MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ae531528f83f3731b4449c7aba012f3228edd9a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103902998"
---
# <a name="midl-compiler-errors-and-warnings"></a>Errores y advertencias del compilador de MIDL

Al utilizar el compilador MIDL, los errores y las advertencias pueden deberse a un uso inadecuado de los modificadores de la línea de comandos o al contenido de los archivos IDL y ACF. Si el error se debe a la entrada incorrecta de los modificadores de la línea de comandos, un mensaje de error o advertencia puede especificar el nombre de uno o varios modificadores de modo de compilador de MIDL. Por ejemplo, puede incluir ciertos atributos ACF en un archivo IDL al usar el modificador de **\_ configuración/App** , pero ese archivo IDL generará un error si se compila sin usar el modificador de **\_ configuración/App** .

Los errores de los archivos IDL y ACF se dividen en dos categorías: errores detectados por el preprocesador y errores reconocidos por el compilador. En esta sección se enumeran los mensajes de error del compilador y el preprocesador de MIDL. También se describen sus formatos y causas.

-   [Formatos de mensajes de error y ADVERTENCIA](error-and-warning-message-formats.md)
-   [Errores de preprocesador](preprocessor-errors.md)
-   [Errores del compilador](compiler-errors.md)

 

 




