---
title: Herramienta de Command-Line MkTypLib
description: MkTypLib es una aplicación de línea de comandos que procesa un archivo IDL para generar una biblioteca de tipos. También se puede usar para generar un archivo de encabezado de C o C++.
ms.assetid: 883d380d-1d73-439b-9f11-ee89fc62fdfd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b712ed8220dd609dd3ba189bdac6b5ee11d2805f26ff5a1f146c20f17c1f8ab9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047943"
---
# <a name="mktyplib-command-line-tool"></a>Herramienta de Command-Line MkTypLib

\[La Mktyplib.exe está obsoleta. En su lugar, use el compilador MIDL. Si necesita compatibilidad con versiones anteriores con programas de Automation antiguos, use el compilador MIDL con la **opción /mktyplib203.**\]

MkTypLib es una aplicación de línea de comandos que procesa un archivo IDL para generar una biblioteca de tipos. También se puede usar para generar un archivo de encabezado de C o C++.

Para generar una biblioteca de tipos a partir de un archivo ODL:

-   En el símbolo del sistema, ejecute el siguiente comando:

    **mktyplibÂ**_filename_

    donde *filename* es el nombre del archivo ODL.

MkTypLib también admite varios parámetros opcionales. Para obtener una lista completa, ejecute la siguiente línea de comandos:

**mktyplib /?**

Dado que MkTypLib es una aplicación obsoleta, no puede analizar archivos IDL o archivos con interfaces definidas fuera de una instrucción [**de**](/windows/desktop/Midl/library) biblioteca. Para obtener más información, vea [Diferencias entre MIDL y MkTypLib.](/windows/desktop/Midl/differences-between-midl-and-mktyplib)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Traducción a C++](translating-to-c--.md)
</dt> </dl>

 

 