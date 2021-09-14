---
description: Windows 7 presenta bibliotecas, que proporcionan a los usuarios una vista única y coherente de sus archivos, incluso cuando esos archivos se almacenan en ubicaciones diferentes.
title: Windows Bibliotecas
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 19DA68B2-FCB6-443d-A3CD-0BF2F429B149
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: ddb21b4678005d3def5812258a75f2e4fec4b9f2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127256995"
---
# <a name="windows-libraries"></a>Windows Bibliotecas

Windows 7 presenta bibliotecas, que proporcionan a los usuarios una vista única y coherente de sus archivos, incluso cuando esos archivos se almacenan en ubicaciones diferentes. Un usuario puede configurar y organizar las bibliotecas, y una biblioteca puede contener carpetas que se encuentran en el equipo del usuario y también carpetas que se han compartido a través de una red. Las bibliotecas presentan una vista más sencilla del sistema de almacenamiento subyacente porque, para el usuario, los archivos y carpetas de una biblioteca se muestran en una sola vista, independientemente de dónde estén almacenados físicamente.

Se recomienda a los desarrolladores que escriban nuevos programas en Windows 7 que usen bibliotecas como medio a través del cual los usuarios interactúan con los archivos utilizados por el programa. El uso de bibliotecas en el programa proporcionará a los usuarios una experiencia más limpia, sencilla y coherente en Windows 7.

Los desarrolladores también deben revisar sus programas existentes y actualizarlos si es necesario para trabajar con bibliotecas. Dado que las bibliotecas no forman parte del sistema de archivos, las API basadas en el sistema de archivos no tendrán acceso a las bibliotecas que el usuario pueda haber configurado.

Los programas que actualmente permiten a los usuarios almacenar su contenido en carpetas diferentes o en equipos diferentes se beneficiarán más cuando agreguen compatibilidad con bibliotecas. Las bibliotecas simplifican la administración de contenido en diversas ubicaciones de almacenamiento para el desarrollador y el usuario.

En esta guía se describe más sobre qué son las bibliotecas, cómo se pueden crear programas para trabajar con bibliotecas y algunas de las formas en que un programa puede usar bibliotecas para mejorar la experiencia del usuario.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de las bibliotecas](library-leverage-to-manage-folders.md)
</dt> <dt>

[Uso de bibliotecas en el programa](library-be-library-aware.md)
</dt> <dt>

[**IShellLibrary**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary)
</dt> <dt>

[Vínculos de shell](./links.md)
</dt> <dt>

[Carpetas conocidas](known-folders.md)
</dt> <dt>

[Esquema de descripción de biblioteca](library-schema-entry.md)
</dt> </dl>

 

 
