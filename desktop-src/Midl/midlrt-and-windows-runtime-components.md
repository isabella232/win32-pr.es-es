---
title: Componentes de MIDLRT y Windows Runtime
description: Muestra cómo crear archivos de metadatos (. winmd) que representan la API de los componentes de Windows Runtime personalizados.
ms.assetid: 7830A5DB-9696-4A93-948B-51DA46A5143C
keywords:
- MIDL del compilador MIDL
- MIDL del compilador MIDL, MIDL y Windows Runtime winrt
- Windows Runtime MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4edf4d40b3fc5b0a5ed8eeb9b5fd47a3b87c4543
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "104533603"
---
# <a name="midlrt-and-windows-runtime-components"></a>Componentes de MIDLRT y Windows Runtime

Muestra cómo crear archivos de metadatos (. winmd) que representan la API de los componentes de Windows Runtime personalizados.


Use el compilador MIDLRT para compilar archivos de metadatos (. winmd) para los componentes de Windows Runtime personalizados.

Cuando se generan los archivos de metadatos, puede crearlos en un paquete más eficaz mediante la utilidad MDMERGE. Para obtener más información, vea [MDMERGE and Metadata files](mdmerge-and-metadata-files.md).


El uso de MIDLRT es similar al uso del compilador de MIDL. Ejecute MIDLRT desde la línea de comandos con el siguiente comando:

**midlrt**  *<* **Opciones** _>_ de **nombre de archivo. idl**

donde *** < *** _>_ representa las opciones de línea de comandos que quiere usar y FILENAME. idl es el nombre del archivo IDL que se va a compilar.


En la lista siguiente se muestran los modificadores de la línea de comandos que usa MIDLRT.EXE.

<dl>

[**/enum ( \_ clase)**](-enum-class.md)  
[**/Metadata \_ dir**](-metadata-dir.md)  
[**/nomidl**](-nomidl.md)  
[**/nomd**](-nomd.md)  
[**/NS ( \_ prefijo)**](-ns-prefix.md)  
[**/winmd**](-winmd.md)  
[**/winrt**](-winrt.md)  
</dl>

Puede encontrar una lista completa de las opciones y los modificadores del compilador de MIDLRT cuando se usa el compilador MIDLRT [**/Help**](-help-.md) y/? centrales. Los modificadores están organizados por categorías. Para obtener más información, vea la [referencia de Command-Line de MIDL](midl-command-line-reference.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Archivos de metadatos y MDMERGE](mdmerge-and-metadata-files.md)
</dt> </dl>

 

 




