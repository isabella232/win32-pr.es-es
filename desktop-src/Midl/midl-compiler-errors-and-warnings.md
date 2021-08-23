---
title: Errores y advertencias del compilador MIDL
description: Cuando se usa el compilador MIDL, los errores y advertencias pueden deberse al uso incorrecto de los modificadores de línea de comandos o al contenido de los archivos IDL y ACF.
ms.assetid: 5c8d5a28-e559-4893-932f-b2306aefa932
keywords:
- Lenguaje de definición de interfaz de Microsoft MIDL , referencia
- MIDL del compilador MIDL, errores
- midl del compilador , errores
- errores MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9f6c2dfd830a1240e2af107eb4a3f1799eafcd0de35ccec7f3756b3e9de5bbf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119146408"
---
# <a name="midl-compiler-errors-and-warnings"></a>Errores y advertencias del compilador MIDL

Cuando se usa el compilador MIDL, los errores y advertencias pueden deberse al uso incorrecto de los modificadores de línea de comandos o al contenido de los archivos IDL y ACF. Si el error se debe a que se escriben incorrectamente los modificadores de la línea de comandos, un mensaje de error o advertencia puede especificar el nombre de uno o varios modificadores de modo del compilador MIDL. Por ejemplo, puede incluir determinados atributos de ACF en un archivo IDL cuando use el modificador **/app \_ config,** pero ese archivo IDL generará un error si compila sin usar el modificador **/app \_ config.**

Los errores de los archivos IDL y ACF se divide en dos categorías: los errores detectados por el preprocesador y los errores reconocidos por el compilador. En esta sección se enumeran los mensajes de error del compilador y el preprocesador MIDL. También describe sus formatos y causas.

-   [Formatos de mensaje de error y advertencia](error-and-warning-message-formats.md)
-   [Errores de preprocesador](preprocessor-errors.md)
-   [Errores del compilador](compiler-errors.md)

 

 




