---
title: Archivos de metadatos y MDMERGE
description: Compone varios archivos de metadatos (. winmd) en una serie de archivos de metadatos de salida, basados en el espacio de nombres.
ms.assetid: A3203627-82DF-4744-BBBC-53D13F30210E
keywords:
- metadata
- archivo winmd
- Metadatos de Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2d91f8c7506dd80fd2477beb61c5b99a26b05b0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103993961"
---
# <a name="mdmerge-and-metadata-files"></a>Archivos de metadatos y MDMERGE

Compone varios archivos de metadatos (. winmd) en una serie de archivos de metadatos de salida, basados en el espacio de nombres.

## <a name="usage"></a>Uso

Ejecute MDMERGE desde la línea de comandos con el siguiente comando:

 *< ***Opciones*** de mdmerge>*

donde *< ***Options*** >* representa las opciones de línea de comandos que desea utilizar.

Genere archivos de metadatos para los componentes de Windows Runtime personalizados mediante el compilador MIDLRT. Para obtener más información, consulte [MIDLRT y Windows Runtime componentes](midlrt-and-windows-runtime-components.md).

## <a name="command-line-switches"></a>Modificadores de línea de comandos

En la lista siguiente se muestran los modificadores de la línea de comandos que usa MDMERGE.

<dl>

[**/i**](-mdmerge-i.md)  
[**/Metadata \_ dir**](-mdmerge-metadata-dir.md)  
[**/n**](-mdmerge-n.md)  
[**/o**](-mdmerge-o.md)  
[**/partial**](-mdmerge-partial.md)  
[**/v**](-mdmerge-v.md)  
</dl>

Puede encontrar una lista completa de las opciones y los modificadores del compilador de MDMERGE cuando se usa la opción **-h** y **/?** centrales.

## <a name="remarks"></a>Observaciones

La composición de metadatos permite que varios archivos IDL contengan definiciones para Windows Runtime componentes en el mismo espacio de nombres. Esto le libera de definir todos los tipos en un espacio de nombres dentro de un solo archivo IDL.

Es probable que tenga numerosos componentes de Windows Runtime que usan las aplicaciones. Cuando realice el paso final para generar ensamblados de metadatos de Windows Runtime que se pueden implementar, puede configurar MDMERGE para combinar componentes de varios directorios de metadatos, como los que se instalan con el sistema (% WINDOWS% \\ system32 \\ WinMetadata), los tipos de base y el directorio de compilación del proyecto actual. Todos los tipos necesarios se combinan en los ensamblados de metadatos correctos e implementables que puede empaquetar para la tienda Windows.

Puede usar la opción [**/n**](-mdmerge-n.md) para especificar la profundidad de espacio de nombres admitida para la composición de ensamblados de metadatos. Esto permite configurar una división activa para los componentes de Windows Runtime, de modo que solo se empaqueta un archivo. winmd único en lugar de muchos. Esto reduce los tiempos de carga y e/s de archivo requeridos por las aplicaciones de la tienda Windows.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Componentes de MIDLRT y Windows Runtime](midlrt-and-windows-runtime-components.md)
</dt> </dl>

 

 




