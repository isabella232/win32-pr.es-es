---
title: MkTypLib Command-Line Tool
description: MkTypLib es una aplicación de línea de comandos que procesa un archivo IDL para generar una biblioteca de tipos. También se puede usar para generar un archivo de encabezado de C o C++.
ms.assetid: 883d380d-1d73-439b-9f11-ee89fc62fdfd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abc392351327124777c2d52d0bbe0653853dcb52
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126889004"
---
# <a name="mktyplib-command-line-tool"></a>MkTypLib Command-Line Tool

\[La Mktyplib.exe está obsoleta. En su lugar, use el compilador MIDL. Si necesita compatibilidad con versiones anteriores con programas de Automation antiguos, use el compilador MIDL con **la opción /mktyplib203.**\]

MkTypLib es una aplicación de línea de comandos que procesa un archivo IDL para generar una biblioteca de tipos. También se puede usar para generar un archivo de encabezado de C o C++.

Para generar una biblioteca de tipos a partir de un archivo ODL:

-   Desde el símbolo del sistema, ejecute el siguiente comando:

    **mktyplibÂ **_filename_

    donde *filename* es el nombre del archivo ODL.

MkTypLib también admite varios parámetros opcionales. Para obtener una lista completa, ejecute la siguiente línea de comandos:

**mktyplib /?**

Dado que MkTypLib es una aplicación obsoleta, no puede analizar archivos IDL ni archivos con interfaces definidas fuera de una instrucción [**de**](/windows/desktop/Midl/library) biblioteca. Para obtener más información, vea [Diferencias entre MIDL y MkTypLib.](/windows/desktop/Midl/differences-between-midl-and-mktyplib)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Traducción a C++](translating-to-c--.md)
</dt> </dl>

 

 