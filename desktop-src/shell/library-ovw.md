---
description: Windows 7 incluye bibliotecas, que proporcionan a los usuarios una vista única y coherente de sus archivos, incluso cuando estos archivos se almacenan en ubicaciones diferentes.
title: Bibliotecas de Windows
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 19DA68B2-FCB6-443d-A3CD-0BF2F429B149
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: ddb21b4678005d3def5812258a75f2e4fec4b9f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104986127"
---
# <a name="windows-libraries"></a>Bibliotecas de Windows

Windows 7 incluye bibliotecas, que proporcionan a los usuarios una vista única y coherente de sus archivos, incluso cuando estos archivos se almacenan en ubicaciones diferentes. Las bibliotecas pueden ser configuradas y organizadas por un usuario, y una biblioteca puede contener carpetas que se encuentran en el equipo del usuario y también carpetas que se han compartido a través de una red. Las bibliotecas presentan una vista más sencilla del sistema de almacenamiento subyacente porque, para el usuario, los archivos y las carpetas de una biblioteca se muestran en una sola vista, independientemente de dónde se almacenen físicamente.

Se recomienda a los desarrolladores que escriban nuevos programas en Windows 7 que usen las bibliotecas como medio para que los usuarios interactúen con los archivos utilizados por el programa. El uso de bibliotecas en el programa proporcionará a los usuarios una experiencia más limpia, más sencilla y más coherente en Windows 7.

Los desarrolladores también deben revisar sus programas existentes y actualizarlos si es necesario, para trabajar con las bibliotecas. Dado que las bibliotecas no forman parte del sistema de archivos, las API basadas en el sistema de archivos no tendrán acceso a las bibliotecas que el usuario podría haber configurado.

Los programas que actualmente permiten a los usuarios almacenar su contenido en carpetas diferentes o en equipos diferentes se beneficiarán de la mayor parte cuando agreguen compatibilidad con la biblioteca. Las bibliotecas simplifican la administración de contenido en diferentes ubicaciones de almacenamiento para el desarrollador y el usuario.

En esta guía se describe más sobre qué son las bibliotecas, cómo se pueden hacer los programas para trabajar con las bibliotecas y algunas de las formas en que un programa puede usar las bibliotecas para mejorar la experiencia del usuario.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de las bibliotecas](library-leverage-to-manage-folders.md)
</dt> <dt>

[Usar bibliotecas en el programa](library-be-library-aware.md)
</dt> <dt>

[**IShellLibrary**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary)
</dt> <dt>

[Vínculos de Shell](./links.md)
</dt> <dt>

[Carpetas conocidas](known-folders.md)
</dt> <dt>

[Esquema de descripción de biblioteca](library-schema-entry.md)
</dt> </dl>

 

 
