---
title: MDMERGE y archivos de metadatos
description: Compone varios archivos de metadatos (.winmd) en una serie de archivos de metadatos de salida, según el espacio de nombres .
ms.assetid: A3203627-82DF-4744-BBBC-53D13F30210E
keywords:
- metadata
- Archivo winmd
- Metadatos de Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a065a8ff93485728b1c5c4c0c7b43de88e3844a8a013f07caee8d85d76d721d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119252435"
---
# <a name="mdmerge-and-metadata-files"></a>MDMERGE y archivos de metadatos

Compone varios archivos de metadatos (.winmd) en una serie de archivos de metadatos de salida, según el espacio de nombres .

## <a name="usage"></a>Uso

Ejecute MDMERGE desde la línea de comandos con el siguiente comando:

**mdmerge**  *<* **opciones**_>_

donde *<***representa** las opciones de línea de _>_ comandos que desea usar.

Genere archivos de metadatos para los componentes Windows runtime personalizados mediante el compilador MIDLRT. Para obtener más información, vea [MIDLRT y Windows Runtime](midlrt-and-windows-runtime-components.md).

## <a name="command-line-switches"></a>Modificadores de línea de comandos

En la lista siguiente se muestran los modificadores de línea de comandos que usa MDMERGE.

<dl>

[**/i**](-mdmerge-i.md)  
[**/metadata \_ dir**](-mdmerge-metadata-dir.md)  
[**/n**](-mdmerge-n.md)  
[**/o**](-mdmerge-o.md)  
[**/partial**](-mdmerge-partial.md)  
[**/v**](-mdmerge-v.md)  
</dl>

Hay disponible una lista completa de las opciones y los modificadores del compilador MDMERGE cuando se usa **-h** y **/?** Interruptores.

## <a name="remarks"></a>Observaciones

La composición de metadatos permite que varios archivos IDL contengan definiciones para Windows runtime en el mismo espacio de nombres. Esto le permite definir todos los tipos de un espacio de nombres dentro de un único archivo IDL.

Es probable que tenga numerosos componentes de Windows runtime que usan las aplicaciones. Al realizar el paso final para generar ensamblados de metadatos de Windows Runtime implementables, puede configurar MDMERGE para combinar componentes de varios directorios de metadatos, como los que se instalan con el sistema (%WINDOWS% \\ system32 WinMetadata), los tipos de base y el directorio de compilación del proyecto \\ actual. Todos los tipos necesarios se combinan en los ensamblados de metadatos correctos e implementables que puede empaquetar para Windows Store.

Puede usar la opción [**/n para**](-mdmerge-n.md) especificar la profundidad de espacio de nombres admitida para crear ensamblados de metadatos. Esto permite configurar una división activa para los componentes de Windows Runtime, de modo que solo se empaquete un único archivo .winmd en lugar de muchos. Esto reduce los tiempos de carga y la E/S de archivo que requieren las aplicaciones Windows Store.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[MIDLRT y componentes Windows runtime](midlrt-and-windows-runtime-components.md)
</dt> </dl>

 

 




