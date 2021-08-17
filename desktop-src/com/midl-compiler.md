---
title: Compilador midl
description: Compilador midl
ms.assetid: ce3d40b7-49fd-4689-9100-fdbad4f0c557
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1db4afbbe8c7a82f4335855b40e578fe2eea046fa4c7f0560e3e297b559a67ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117736434"
---
# <a name="midl-compiler"></a>Compilador midl

El compilador MIDL procesa un archivo IDL para generar una biblioteca de tipos y archivos de salida. El tipo de archivos de salida generados por el compilador MIDL depende de los atributos especificados en la lista de atributos de interfaz del archivo IDL.

Si la lista de atributos contiene la palabra clave object, el compilador MIDL genera archivos de salida de interfaz COM: un archivo de proxy de interfaz, un archivo de encabezado de interfaz y un archivo de identificador único \[ [](/windows/desktop/Midl/object) \] global (GUID) para la interfaz. Si el archivo IDL contiene una instrucción [**de**](/windows/desktop/Midl/library) biblioteca, MIDL genera un archivo de biblioteca de tipos con la extensión de nombre de archivo .tlb. Si hay interfaces en el archivo IDL que no tienen la palabra clave object y no están incluidas en una instrucción de biblioteca, el compilador MIDL genera archivos de salida de interfaz adecuados para las llamadas a procedimiento remoto (RPC): un archivo de código auxiliar de cliente, un archivo de código auxiliar de servidor y un archivo de \[  \] encabezado.  Para obtener más información, vea los temas [Interface Definitions and Type Libraries (Definiciones](/windows/desktop/Midl/interface-definitions-and-type-libraries) de interfaz y bibliotecas de tipos) y [Generating a Type Library with MIDL (Generación de una biblioteca de tipos con MIDL).](/windows/desktop/Midl/generating-a-type-library-with-midl-2)

Para generar una biblioteca de tipos y archivos de salida a partir de un archivo IDL:

-   Desde el símbolo del sistema, ejecute

    **midl** *filename*

    donde *filename* es el nombre del archivo IDL.

El compilador midl también admite varios parámetros opcionales. Para obtener una lista completa, vea "MIDL Command-Line Reference" en la documentación Visual C++ o ejecute la siguiente línea de comandos:

**midl /?**

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Lenguaje de definición de interfaz de Microsoft](/windows/desktop/Midl/midl-start-page)
</dt> <dt>

[Traducción a C++](translating-to-c--.md)
</dt> </dl>

 

 