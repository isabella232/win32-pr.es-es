---
description: Para NLS, ordenación (también conocida como &\# 0034;intercalación&\# 0034;) es la organización de cadenas.
ms.assetid: 8ca3af60-1ddb-4bfb-8aa6-8db769b3982d
title: Ordenación (internacionalización)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3dbedf872c953a45ca7064eccd4ba16019a857c35186261695e094be03cd054
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120130215"
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

 

 
