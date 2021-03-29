---
title: Acerca de los archivos de recursos
description: Describe cómo incluir recursos en una aplicación basada en Windows con RC.
ms.assetid: af7c7aed-5d28-40ac-ad00-da0986fd89c1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c43e9df59cf0b6507b6c6a53c42299b8792634f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075727"
---
# <a name="about-resource-files"></a>Acerca de los archivos de recursos

Para incluir recursos en la aplicación basada en Windows con RC, haga lo siguiente:

1.  Cree archivos individuales para los cursores, iconos, mapas de bits, cuadros de diálogo y fuentes.
2.  Cree un script de definición de recursos (archivo. RC) que describa los recursos utilizados por la aplicación.
3.  Compile el script con RC. Para obtener más información, consulte [uso de RC (la línea de comandos de RC)](using-rc-the-rc-command-line-.md).
4.  Vincule el archivo de recursos compilado (. res) al archivo ejecutable de la aplicación con el enlazador.

Un archivo de recursos es un archivo de texto con la extensión. rc. El archivo puede utilizar caracteres de un solo byte, de doble byte o Unicode. La sintaxis y la semántica del preprocesador RC son similares a las del compilador de C/C++ de Microsoft. Sin embargo, RC admite un subconjunto de las directivas de preprocesador, define y pragma en un script.

El archivo de script define los recursos. En el caso de un recurso que se encuentre en un archivo independiente, como un icono o un cursor, el script especifica el recurso y el archivo que lo contiene. En algunos recursos, como un menú, la definición completa del recurso existe en el script.

En los temas siguientes se describe la información que puede contener un archivo de script:

-   [Comentarios](comments.md), que son notas que RC omitirá.
-   [Macros predefinidas](predefined-macros.md), que no toman ningún argumento y no se pueden redefinir.
-   [Directivas de preprocesador](preprocessor-directives.md), que indican a RC que realice acciones en el script antes de compilarlo.
-   [Operadores de preprocesador](preprocessor-operators.md), que se usan con la Directiva de **\# definición** .
-   [Directivas pragma](pragma-directives.md)
-   [Instrucciones de definición de recursos](resource-definition-statements.md), que denominan y describen los recursos.

 

 




