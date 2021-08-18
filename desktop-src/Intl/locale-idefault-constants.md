---
description: En este tema se definen las constantes \_ IDEFAULT de LOCALE \* que usa NLS.
ms.assetid: 4fa8b5f3-8c01-44fb-b6fd-8dbf38e3d361
title: LOCALE_IDEFAULT* Constantes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0524ea64d9924439e14ae6cb3cf16fed8a5f97ffb1e95d5f7fea98d5b6c61329
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120106785"
---
# <a name="locale_idefault-constants"></a>Constantes \_ IDEFAULT de LOCALE \*

En este tema se definen las constantes \_ IDEFAULT de LOCALE \* que usa NLS.



| Value                          | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|--------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CONFIGURACIÓN REGIONAL \_ IDEFAULTANSICODEPAGE   | Página de códigos ANSI utilizada por una configuración regional para aplicaciones que no admiten Unicode. El número máximo de caracteres permitido para esta cadena es seis, incluido un carácter nulo de terminación. Si no hay ninguna página de códigos ANSI disponible, solo se puede usar Unicode para la configuración regional. En este caso, el valor es CP \_ ACP (0). Esta configuración regional no se puede establecer como configuración regional del sistema. Las aplicaciones que no admiten Unicode no funcionan correctamente con configuraciones regionales marcadas como "Solo Unicode". Para obtener una lista de ANSI y otras páginas de códigos, vea [Identificadores de página de códigos](code-page-identifiers.md). |
| CONFIGURACIÓN REGIONAL \_ IDEFAULTCODEPAGE       | Página de códigos del fabricante de equipos originales (OEM) asociada al país o región. La página de códigos de OEM se usa para la conversión de aplicaciones en modo de texto basadas en MS-DOS. Si la configuración regional no usa una página de códigos oem, el valor es CP \_ OEMCP (1). El número máximo de caracteres permitido para esta cadena es seis, incluido un carácter nulo de terminación. Para obtener una lista de OEM y otras páginas de códigos, vea [Identificadores de página de códigos](code-page-identifiers.md).                                                                                                               |
| LOCALE \_ IDEFAULTCOUNTRY        | Obsoleto. No debe usarse. Este valor se proporcionó para que las configuraciones regionales especificadas parcialmente se pudieran completar con valores predeterminados. Las configuraciones regionales parcialmente especificadas ahora están en desuso.                                                                                                                                                                                                                                                                                                                                                                                               |
| CONFIGURACIÓN REGIONAL \_ IDEFAULTEBCDICCODEPAGE | **Windows 2000:** Página Extended Binary Coded Decimal Interchange Code de códigos predeterminada (EBCDIC) asociada a la configuración regional. El número máximo de caracteres permitido para esta cadena es seis, incluido un carácter nulo de terminación. Para obtener una lista de EBCDIC y otras páginas de códigos, vea [Identificadores de página de códigos](code-page-identifiers.md).                                                                                                                                                                                                                                     |
| CONFIGURACIÓN REGIONAL \_ IDEFAULTLANGUAGE       | Obsoleto. No debe usarse. Este valor se proporcionó para que las configuraciones regionales especificadas parcialmente se pudieran completar con valores predeterminados. Las configuraciones regionales parcialmente especificadas ahora están en desuso.                                                                                                                                                                                                                                                                                                                                                                                               |
| CONFIGURACIÓN REGIONAL \_ IDEFAULTMACCODEPAGE    | Página de códigos de Macintosh predeterminada asociada a la configuración regional. El número máximo de caracteres permitido para esta cadena es seis, incluido un carácter nulo de terminación. Si la configuración regional no usa una página de códigos de Macintosh, el valor es CP \_ MACCP (2). Para obtener una lista de Macintosh (MAC) y otras páginas de códigos, vea [Identificadores de página de códigos](code-page-identifiers.md).                                                                                                                                                                                                              |



 

 

 



