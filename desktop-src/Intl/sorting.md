---
description: Para NLS, ordenación (también conocida como &\# 0034;intercalación&\# 0034;). es la organización de cadenas.
ms.assetid: 8ca3af60-1ddb-4bfb-8aa6-8db769b3982d
title: Ordenación (internacionalización)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f49a5abb8371a00ad9ee63f929b4aaf4b18b11be
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127171929"
---
# <a name="sorting"></a>Ordenación

Para NLS, la ordenación (también conocida como "intercalación") es la organización de cadenas. Hay dos tipos de ordenación:

-   Ordenación lingüística. Organiza cadenas con características lingüísticas similares en grupos (por ordenaciones).
-   Ordenación ordinal (no lingüística). Organiza las cadenas en una secuencia ordenada.

La ordenación usa las funciones de comparación de cadenas NLS, como [CompareString](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) y [**LCMapString,**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa)o funciones de API de "contenedor", como [lstrcmp](/windows/win32/api/winbase/nf-winbase-lstrcmpa), que llaman internamente a las funciones de comparación de cadenas NLS.

Para obtener más información sobre cómo implementar la ordenación en las aplicaciones, consulte [Control de la ordenación en las aplicaciones.](handling-sorting-in-your-applications.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de la compatibilidad con idiomas nacionales](about-national-language-support.md)
</dt> <dt>

[Control de la ordenación en las aplicaciones](handling-sorting-in-your-applications.md)
</dt> <dt>

[**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw)
</dt> <dt>

[LCMapString](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa)
</dt> </dl>

 

 
