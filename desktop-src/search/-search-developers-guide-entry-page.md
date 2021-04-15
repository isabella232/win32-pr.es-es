---
description: Los terceros pueden crear aplicaciones que consultan los datos en el índice mediante programación y pueden extender la búsqueda de Windows para indizar los datos de los formatos de archivo y los almacenes de datos personalizados.
ms.assetid: 70046df0-ce48-472d-b24b-8231ea3a43c0
title: Guía del desarrollador de Windows Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61593f47e081059966936a99a7d2baea114df92a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497086"
---
# <a name="windows-search-developers-guide"></a>Guía del desarrollador de Windows Search

Los terceros pueden crear aplicaciones que consultan los datos en el índice mediante programación y pueden extender la búsqueda de Windows para indizar los datos de los formatos de archivo y los almacenes de datos personalizados. Para crear aplicaciones de Windows Search, los desarrolladores de terceros deben implementar primero un almacén de datos de Shell para lograr una experiencia de usuario razonable. Para obtener más información, vea [implementar las interfaces de objeto de carpeta básicas](/previous-versions/windows/desktop/legacy/cc144093(v=vs.85)).

También debe descargar el [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) de las bibliotecas de Windows Search. Los [ejemplos del SDK de Windows Search](https://www.microsoft.com/downloads/details.aspx?FamilyID=645300AE-5E7A-4CE7-95F0-49793F8F76E8) contienen ejemplos de código útiles y un ensamblado de interoperabilidad para desarrollar con código administrado. Para obtener más información sobre el uso de los ejemplos de código, vea [ejemplos de código de Windows Search](-search-3x-wds-sampleentry.md).

Esta sección está organizada de la siguiente manera:

- [Administración del índice](-search-3x-wds-mngidx-overview.md)
- [Consulta del índice mediante programación](-search-3x-wds-qryidx-overview.md)
- [Extender el índice](-search-3x-wds-extidx-overview.md)
- [Extensión de recursos de idioma](extending-language-resources-in-windows-search.md)

## <a name="additional-resources"></a>Recursos adicionales

- Para ver los paneles de mensajes de preguntas y debate admitidos por la comunidad en tecnologías de búsqueda, vea [Foro de MSDN: desarrollo de Windows Desktop Search](https://social.msdn.microsoft.com/Forums/windowsdesktopsearchdevelopment/threads).
- Para descargar los ejemplos de código de búsqueda:
  - [Ejemplos de Windows Search](-search-samples-ovw.md)
- Para descargar el Windows SDK:
  - Para Windows 10: [SDK de Windows 10](https://developer.microsoft.com/windows/downloads/windows-10-sdk)
  - Para Windows 7: [Windows SDK para Windows 7 y .NET Framework](https://msdn.microsoft.com/windowsvista/bb980924.aspx)

## <a name="related-topics"></a>Temas relacionados

[Información general sobre Windows Search](-search-3x-wds-overview.md)

[Referencia de Windows Search](-search-reference-entry-page.md)

[Ejemplos de código de Windows Search](-search-samples-ovw.md)

[Búsqueda federada en Windows](-search-federated-search-overview.md)

[Tecnologías de búsqueda relacionadas](-search-3x-wds-sampleentry.md)

[Glosario de búsqueda de Windows](search-glossary.md)
