---
title: Compilador midl
description: Compilador midl
ms.assetid: ce3d40b7-49fd-4689-9100-fdbad4f0c557
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fa57131e31e9c6273270a771f9ba862d73bc142
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126889028"
---
# <a name="midl-compiler"></a>Compilador midl

El compilador MIDL procesa un archivo IDL para generar una biblioteca de tipos y archivos de salida. El tipo de archivos de salida generados por el compilador MIDL depende de los atributos especificados en la lista de atributos de interfaz del archivo IDL.

Si la lista de atributos contiene la palabra clave object, el compilador MIDL genera archivos de salida de interfaz COM: un archivo de proxy de interfaz, un archivo de encabezado de interfaz y un archivo de identificador único \[ [](/windows/desktop/Midl/object) \] global (GUID) para la interfaz. Si el archivo IDL contiene una instrucción [**de**](/windows/desktop/Midl/library) biblioteca, MIDL genera un archivo de biblioteca de tipos con la extensión de nombre de archivo .tlb. Si hay interfaces en el archivo IDL que no tienen la palabra clave object y no están incluidas en una instrucción de biblioteca, el compilador MIDL genera archivos de salida de interfaz adecuados para las llamadas a procedimiento remoto (RPC): un archivo de código auxiliar de cliente, un archivo de código auxiliar de servidor y un archivo de \[  \] encabezado.  Para obtener más información, vea los temas [Interface Definitions and Type Libraries (Definiciones](/windows/desktop/Midl/interface-definitions-and-type-libraries) de interfaz y bibliotecas de tipos) y [Generating a Type Library with MIDL (Generación de una biblioteca de tipos con MIDL).](/windows/desktop/Midl/generating-a-type-library-with-midl-2)

Para generar una biblioteca de tipos y archivos de salida a partir de un archivo IDL:

-   Desde el símbolo del sistema, ejecute

    **midl** *filename*

    donde *filename* es el nombre del archivo IDL.

El compilador midl también admite varios parámetros opcionales. Para obtener una lista completa, vea "MIDL Command-Line Reference" (Referencia de Command-Line MIDL) en la documentación Visual C++ o ejecute la siguiente línea de comandos:

**midl /?**

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Lenguaje de definición de interfaz de Microsoft](/windows/desktop/Midl/midl-start-page)
</dt> <dt>

[Traducción a C++](translating-to-c--.md)
</dt> </dl>

 

 