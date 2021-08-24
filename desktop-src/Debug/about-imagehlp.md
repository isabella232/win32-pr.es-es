---
description: Las funciones ImageHlp se usan principalmente mediante herramientas de programación, utilidades de configuración de aplicaciones y otros programas que necesitan acceso a los datos contenidos en una imagen de PE.
ms.assetid: 831d7bb2-bf01-4422-a940-173f9856a513
title: Acerca de ImageHlp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4aee63eba22293fe1fb56cb6608110f4343a0c6bc26a4be597bfbd884cdf87cd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119815655"
---
# <a name="about-imagehlp"></a>Acerca de ImageHlp

Las funciones ImageHlp se usan principalmente mediante herramientas de programación, utilidades de configuración de aplicaciones y otros programas que necesitan acceso a los datos contenidos en una imagen de PE. Todas las funciones ImageHlp son de un solo subproceso. Por lo tanto, las llamadas desde más de un subproceso a esta función probablemente darán lugar a un comportamiento inesperado o daños en la memoria. Para evitarlo, debe sincronizar todas las llamadas simultáneas de más de un subproceso a esta función.

En los temas siguientes se describen las imágenes pe y la funcionalidad proporcionada por las funciones ImageHlp.

-   [Formato PE](pe-format.md)
-   [Funciones de acceso a imágenes](image-access-functions.md)
-   [Funciones de integridad de imágenes](image-integrity-functions.md)
-   [Funciones de modificación de imágenes](image-modification-functions.md)

 

 



