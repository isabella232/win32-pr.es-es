---
title: Acerca de los archivos de recursos
description: Describe cómo incluir recursos en la aplicación basada Windows con RC.
ms.assetid: af7c7aed-5d28-40ac-ad00-da0986fd89c1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c43e9df59cf0b6507b6c6a53c42299b8792634f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127268580"
---
# <a name="about-resource-files"></a>Acerca de los archivos de recursos

Para incluir recursos en la Windows basada en aplicaciones con RC, haga lo siguiente:

1.  Cree archivos individuales para los cursores, iconos, mapas de bits, cuadros de diálogo y fuentes.
2.  Cree un script de definición de recursos (archivo .rc) que describa los recursos usados por la aplicación.
3.  Compile el script con RC. Para obtener más información, [vea Using RC (The RC Command Line)](using-rc-the-rc-command-line-.md).
4.  Vincule el archivo de recursos compilados (.res) al archivo ejecutable de la aplicación con el vinculador.

Un archivo de recursos es un archivo de texto con la extensión .rc. El archivo puede usar caracteres Unicode, de un solo byte o de doble byte. La sintaxis y la semántica del preprocesador RC son similares a las del compilador de Microsoft C/C++. Sin embargo, RC admite un subconjunto de las directivas de preprocesador, define y pragmas en un script.

El archivo de script define los recursos. Para un recurso que existe en un archivo independiente, como un icono o cursor, el script especifica el recurso y el archivo que lo contiene. Para algunos recursos, como un menú, toda la definición del recurso existe dentro del script.

En los temas siguientes se describe la información que puede contener un archivo de script:

-   [Comentarios](comments.md), que son notas que RC debe omitir.
-   [Macros predefinidas](predefined-macros.md), que no toman ningún argumento y no se pueden volver a definir.
-   [Directivas de preprocesador](preprocessor-directives.md), que indica a RC que realice acciones en el script antes de compilarlo.
-   [Operadores de preprocesador](preprocessor-operators.md), que se usan con la **\# directiva define.**
-   [Directivas pragma](pragma-directives.md)
-   [Instrucciones de definición de recursos](resource-definition-statements.md), que nombren y describen los recursos.

 

 




