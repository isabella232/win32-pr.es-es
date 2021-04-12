---
description: WMI implementa una técnica que permite almacenar varias versiones localizadas de la misma clase en el repositorio.
ms.assetid: 01e1cee5-d882-45b6-ac93-68533c2c6c9d
ms.tgt_platform: multiple
title: Localizar información de clase WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa9f1a7e34c3ba230655ebba4c070981a8dab901
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361278"
---
# <a name="localizing-wmi-class-information"></a>Localizar información de clase WMI

WMI implementa una técnica que permite almacenar varias versiones localizadas de la misma clase en el repositorio.

La definición de clase se divide en las siguientes versiones:

-   Versión independiente del lenguaje que solo contiene una definición de clase básica.
-   Una versión específica del idioma que contiene información localizada, como descripciones de propiedades específicas de una configuración regional.

Las definiciones de clase específicas del lenguaje se almacenan en un espacio de nombres secundario debajo del espacio de nombres que contiene una definición de clase básica independiente del lenguaje.

Cuando se solicita una definición de clase localizada para una configuración regional específica, WMI combina la definición de clase básica y la información de clase localizada para formar una clase localizada completa. Puede obtener una versión localizada de una clase WMI si especifica una configuración regional cuando se conecta a WMI y establece una marca que indica que desea información localizada. Después, WMI combina la información de la versión independiente del lenguaje y de las versiones específicas del lenguaje de la definición de clase para formar una clase localizada.

Las clases WMI que contienen información localizada se marcan con el calificador de **modificación** y se denominan clases modificadas. una clase admite información localizada si tiene este calificador. Puede determinar la configuración regional para la que se ha localizado la clase comprobando otro calificador denominado [**configuración regional**](swbemobjectpath-locale.md). El calificador de configuración regional contiene un identificador de localización (LCID de Windows) que identifica una configuración regional. Por ejemplo, la configuración regional de inglés americano es 0xC0A. Si un calificador de una clase modificada contiene información localizada, contiene el tipo de calificador **corregido** .

La localización de WMI incluye las siguientes tareas:

-   [Crear definiciones de clase localizadas](creating-localized-class-definitions.md)
-   [Compilar archivos MOF localizados](compiling-localized-mof-files.md)
-   [Localizar valores de propiedad](localizing-property-values.md)
-   [Recuperar clases modificadas](retrieving-amended-classes.md)

Para obtener más información, vea Consideraciones de la [clase modificada](amended-class-considerations.md).

 

 



