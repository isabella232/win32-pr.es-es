---
title: Compilador MIDL
description: Compilador MIDL
ms.assetid: ce3d40b7-49fd-4689-9100-fdbad4f0c557
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fa57131e31e9c6273270a771f9ba862d73bc142
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "103794127"
---
# <a name="midl-compiler"></a>Compilador MIDL

El compilador MIDL procesa un archivo IDL para generar una biblioteca de tipos y archivos de salida. El tipo de archivos de salida generados por el compilador MIDL depende de los atributos especificados en la lista de atributos de interfaz del archivo IDL.

Si la lista de atributos contiene la \[ [](/windows/desktop/Midl/object) \] palabra clave Object, el compilador MIDL genera archivos de salida de la interfaz com: un archivo proxy de interfaz, un archivo de encabezado de interfaz y un archivo de identificador único global (GUID) para la interfaz. Si el archivo IDL contiene una instrucción de [**biblioteca**](/windows/desktop/Midl/library) , MIDL genera un archivo de biblioteca de tipos con la extensión de nombre de archivo. tlb. Si hay interfaces en el archivo IDL que no tienen la \[  \] palabra clave Object y no se incluyen en una instrucción **Library** , el compilador MIDL genera archivos de salida de interfaz adecuados para llamadas a procedimiento remoto (RPC): un archivo de código auxiliar de cliente, un archivo de código auxiliar de servidor y un archivo de encabezado. Para obtener más información, vea los temas sobre [definiciones de interfaz y bibliotecas de tipos](/windows/desktop/Midl/interface-definitions-and-type-libraries) y [generación de una biblioteca de tipos con MIDL](/windows/desktop/Midl/generating-a-type-library-with-midl-2).

Para generar una biblioteca de tipos y archivos de salida a partir de un archivo IDL:

-   En el símbolo del sistema, ejecute

     *nombre de archivo* MIDL

    donde *filename* es el nombre del archivo IDL.

El compilador MIDL también admite varios parámetros opcionales. Para obtener una lista completa, vea "referencia de Command-Line MIDL" en la documentación de Visual C++, o ejecute la siguiente línea de comandos:

**MIDL/?**

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Lenguaje de definición de interfaz de Microsoft](/windows/desktop/Midl/midl-start-page)
</dt> <dt>

[Traducir a C++](translating-to-c--.md)
</dt> </dl>

 

 