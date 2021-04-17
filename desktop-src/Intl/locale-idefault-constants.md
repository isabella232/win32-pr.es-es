---
description: En este tema se definen las constantes de IDEFAULT de configuración regional \_ \* utilizadas por NLS.
ms.assetid: 4fa8b5f3-8c01-44fb-b6fd-8dbf38e3d361
title: Constantes de LOCALE_IDEFAULT *
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf9c440c27a2fe551eae7d03d66cc43b500e8f68
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686497"
---
# <a name="locale_idefault-constants"></a>Constantes de IDEFAULT de configuración regional \_ \*

En este tema se definen las constantes de IDEFAULT de configuración regional \_ \* utilizadas por NLS.



| Value                          | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|--------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| configuración regional \_ IDEFAULTANSICODEPAGE   | Página de códigos ANSI usada por una configuración regional para las aplicaciones que no admiten Unicode. El número máximo de caracteres permitido para esta cadena es seis, incluido un carácter nulo de terminación. Si no hay ninguna página de códigos ANSI disponible, solo se puede usar Unicode para la configuración regional. En este caso, el valor es CP \_ ACP (0). Este tipo de configuración regional no se puede establecer como la configuración regional del sistema. Las aplicaciones que no admiten Unicode no funcionan correctamente con las configuraciones regionales marcadas como "solo Unicode". Para obtener una lista de las páginas de códigos ANSI y otras, vea [identificadores de páginas de códigos](code-page-identifiers.md). |
| configuración regional \_ IDEFAULTCODEPAGE       | Página de códigos del fabricante de equipos originales (OEM) asociada al país o región. La página de códigos OEM se usa para la conversión de aplicaciones de modo de texto basadas en MS-dos. Si la configuración regional no usa una página de códigos OEM, el valor es CP \_ OEMCP (1). El número máximo de caracteres permitido para esta cadena es seis, incluido un carácter nulo de terminación. Para obtener una lista de OEM y otras páginas de códigos, vea [identificadores de páginas de códigos](code-page-identifiers.md).                                                                                                               |
| configuración regional \_ IDEFAULTCOUNTRY        | Obsoleto. No debe usarse. Se proporcionó este valor para que se puedan completar las configuraciones regionales especificadas con valores predeterminados. Las configuraciones regionales especificadas parcialmente ahora están en desuso.                                                                                                                                                                                                                                                                                                                                                                                               |
| configuración regional \_ IDEFAULTEBCDICCODEPAGE | **Windows 2000:** Página de códigos de Extended Binary Coded Decimal Interchange Code predeterminada (EBCDIC) asociada a la configuración regional. El número máximo de caracteres permitido para esta cadena es seis, incluido un carácter nulo de terminación. Para obtener una lista de EBCDIC y otras páginas de códigos, vea [identificadores de páginas de códigos](code-page-identifiers.md).                                                                                                                                                                                                                                     |
| configuración regional \_ IDEFAULTLANGUAGE       | Obsoleto. No debe usarse. Se proporcionó este valor para que se puedan completar las configuraciones regionales especificadas con valores predeterminados. Las configuraciones regionales especificadas parcialmente ahora están en desuso.                                                                                                                                                                                                                                                                                                                                                                                               |
| configuración regional \_ IDEFAULTMACCODEPAGE    | Página de códigos predeterminada de Macintosh asociada a la configuración regional. El número máximo de caracteres permitido para esta cadena es seis, incluido un carácter nulo de terminación. Si la configuración regional no usa una página de códigos de Macintosh, el valor es CP \_ MACCP (2). Para obtener una lista de Macintosh (MAC) y otras páginas de códigos, vea [identificadores de páginas de códigos](code-page-identifiers.md).                                                                                                                                                                                                              |



 

 

 



