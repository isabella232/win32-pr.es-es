---
title: Herramienta de Command-Line MkTypLib
description: MkTypLib es una aplicación de línea de comandos que procesa un archivo IDL para generar una biblioteca de tipos. También se puede utilizar para generar un archivo de encabezado de C o C++.
ms.assetid: 883d380d-1d73-439b-9f11-ee89fc62fdfd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abc392351327124777c2d52d0bbe0653853dcb52
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "103794128"
---
# <a name="mktyplib-command-line-tool"></a>Herramienta de Command-Line MkTypLib

\[La herramienta Mktyplib.exe está obsoleta. En su lugar, utilice el compilador de MIDL. Si necesita compatibilidad con versiones anteriores de los programas de automatización anteriores, utilice el compilador MIDL con la opción **/mktyplib203** .\]

MkTypLib es una aplicación de línea de comandos que procesa un archivo IDL para generar una biblioteca de tipos. También se puede utilizar para generar un archivo de encabezado de C o C++.

Para generar una biblioteca de tipos a partir de un archivo ODL:

-   En el símbolo del sistema, ejecute el siguiente comando:

    **mktyplibÂ * * * nombreDeArchivo*

    donde *filename* es el nombre del archivo ODL.

MkTypLib también admite varios parámetros opcionales. Para obtener una lista completa, ejecute la siguiente línea de comandos:

**MkTypLib/?**

Dado que MkTypLib es una aplicación obsoleta, no puede analizar archivos IDL ni archivos con interfaces definidas fuera de una instrucción [**Library**](/windows/desktop/Midl/library) . Para obtener más información, vea [diferencias entre MIDL y MkTypLib](/windows/desktop/Midl/differences-between-midl-and-mktyplib).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Traducir a C++](translating-to-c--.md)
</dt> </dl>

 

 