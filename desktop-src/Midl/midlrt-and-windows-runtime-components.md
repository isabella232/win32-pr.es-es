---
title: MIDLRT y componentes Windows Runtime
description: Muestra cómo crear archivos de metadatos (.winmd) que representan la API para componentes personalizados Windows runtime.
ms.assetid: 7830A5DB-9696-4A93-948B-51DA46A5143C
keywords:
- MIDL del compilador MIDL
- MIDL del compilador MIDL, MIDL y Windows Runtime winrt
- Windows MIDL en tiempo de ejecución
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f827178216bbb7e78c16f2c11fa68b29b2eb50cfc0714a0ed53b02ce5bdc4ba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118642909"
---
# <a name="midlrt-and-windows-runtime-components"></a>MIDLRT y componentes Windows Runtime

Muestra cómo crear archivos de metadatos (.winmd) que representan la API para componentes personalizados Windows runtime.


Use el compilador MIDLRT para compilar archivos de metadatos (.winmd) para los componentes personalizados Windows runtime.

Cuando se generan los archivos de metadatos, puede crearlos en un paquete más eficaz mediante la utilidad MDMERGE. Para obtener más información, vea [MDMERGE y archivos de metadatos](mdmerge-and-metadata-files.md).


El uso de MIDLRT es similar al uso del compilador MIDL. Ejecute MIDLRT desde la línea de comandos con el siguiente comando:

**midlrt**  *<* **opciones** _>_ **filename.idl**

donde *<* representa las opciones de línea de comandos que desea usar y Filename.idl es el nombre del archivo IDL que se _>_ va a compilar.


En la lista siguiente se muestran los modificadores de línea de comandos que MIDLRT.EXE utiliza.

<dl>

[**/enum \_ (clase)**](-enum-class.md)  
[**/metadata \_ dir**](-metadata-dir.md)  
[**/nomidl**](-nomidl.md)  
[**/nomd**](-nomd.md)  
[**Prefijo \_ /ns**](-ns-prefix.md)  
[**/winmd**](-winmd.md)  
[**/winrt**](-winrt.md)  
</dl>

Al usar el compilador MIDLRT [**/help**](-help-.md) y /? hay disponible una lista completa de las opciones y modificadores del compilador de MIDLRT. Interruptores. Los modificadores se organizan por categorías. Para obtener más información, vea [midl Command-Line referencia](midl-command-line-reference.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[MDMERGE y archivos de metadatos](mdmerge-and-metadata-files.md)
</dt> </dl>

 

 




