---
description: WMI implementa una técnica que permite almacenar varias versiones localizadas de la misma clase en el repositorio.
ms.assetid: 01e1cee5-d882-45b6-ac93-68533c2c6c9d
ms.tgt_platform: multiple
title: Localización de información de clase WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c3784128c48282d05620faf470217b195b26614d81b5b847e7a7a8ad6b9252f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119131217"
---
# <a name="localizing-wmi-class-information"></a>Localización de información de clase WMI

WMI implementa una técnica que permite almacenar varias versiones localizadas de la misma clase en el repositorio.

La definición de clase se divide en las siguientes versiones:

-   Versión neutra del lenguaje que contiene solo una definición de clase básica.
-   Versión específica del idioma que contiene información localizada, como descripciones de propiedades específicas de una configuración regional.

Las definiciones de clase específicas del lenguaje se almacenan en un espacio de nombres secundario debajo del espacio de nombres que contiene una definición de clase básica neutra del lenguaje.

Cuando se solicita una definición de clase localizada para una configuración regional específica, WMI combina la definición de clase básica y la información de clase localizada para formar una clase localizada completa. Puede obtener una versión localizada de una clase WMI especificando una configuración regional al conectarse a WMI y estableciendo una marca que indica que desea información localizada. A continuación, WMI combina la información de las versiones neutras del idioma y específicas del idioma de la definición de clase para formar una clase localizada.

Las clases WMI que contienen información localizada se marcan con el **calificador Amendment** y se denominan clases modificadas; Una clase admite información localizada si tiene este calificador. Puede determinar para qué configuración regional se ha localizado la clase si busca otro calificador denominado [**Configuración regional.**](swbemobjectpath-locale.md) El calificador de configuración regional contiene un identificador de localización (Windows LCID) que identifica una configuración regional. Por ejemplo, la configuración regional del inglés estadounidense es 0x409. Si un calificador de una clase modificada contiene información localizada, contiene el **tipo de calificador** modificado.

La localización wmi incluye las siguientes tareas:

-   [Creación de definiciones de clase localizadas](creating-localized-class-definitions.md)
-   [Compilación de archivos MOF localizados](compiling-localized-mof-files.md)
-   [Localización de valores de propiedad](localizing-property-values.md)
-   [Recuperación de clases modificadas](retrieving-amended-classes.md)

Para obtener más información, vea [Consideraciones de clase modificadas](amended-class-considerations.md).

 

 



