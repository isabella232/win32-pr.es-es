---
description: Para NLS, ordenación (también conocida como &\# 0034; intercalación&\# 0034;) es la disposición de las cadenas.
ms.assetid: 8ca3af60-1ddb-4bfb-8aa6-8db769b3982d
title: Ordenación (internacionalización)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f49a5abb8371a00ad9ee63f929b4aaf4b18b11be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279351"
---
# <a name="sorting"></a>Ordenación

En el caso de NLS, la ordenación (también conocida como "intercalación") es la organización de las cadenas. Hay dos tipos de ordenación:

-   Ordenación lingüística. Organiza las cadenas con características lingüísticas similares en grupos (por orden).
-   Ordenación ordinal (no lingüística). Organiza las cadenas en una secuencia ordenada.

La ordenación utiliza las funciones de comparación de cadenas NLS, como [CompareString](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) y [**LCMapString**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa), o las funciones de la API "wrapper", como [lstrcmp](/windows/win32/api/winbase/nf-winbase-lstrcmpa), que llaman internamente a las funciones de comparación de cadenas NLS.

Para obtener más información sobre la implementación de la ordenación en las aplicaciones, vea [controlar la ordenación en las aplicaciones](handling-sorting-in-your-applications.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de la compatibilidad con National Language](about-national-language-support.md)
</dt> <dt>

[Controlar la ordenación en las aplicaciones](handling-sorting-in-your-applications.md)
</dt> <dt>

[**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw)
</dt> <dt>

[LCMapString](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa)
</dt> </dl>

 

 
