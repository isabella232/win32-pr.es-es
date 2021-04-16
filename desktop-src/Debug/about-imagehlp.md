---
description: Las funciones ImageHlp las usan principalmente las herramientas de programación, las utilidades de instalación de aplicaciones y otros programas que necesitan acceso a los datos contenidos en una imagen PE.
ms.assetid: 831d7bb2-bf01-4422-a940-173f9856a513
title: Acerca de ImageHlp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b76da517a396536640df0e9bfcfa05368e4d0b76
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659429"
---
# <a name="about-imagehlp"></a>Acerca de ImageHlp

Las funciones ImageHlp las usan principalmente las herramientas de programación, las utilidades de instalación de aplicaciones y otros programas que necesitan acceso a los datos contenidos en una imagen PE. Todas las funciones ImageHlp tienen un único subproceso. Por lo tanto, las llamadas desde más de un subproceso a esta función probablemente producirán un comportamiento inesperado o daños en la memoria. Para evitar esto, debe sincronizar todas las llamadas simultáneas de más de un subproceso a esta función.

En los temas siguientes se describen las imágenes PE y la funcionalidad proporcionada por las funciones ImageHlp.

-   [Formato PE](pe-format.md)
-   [Funciones de acceso a imágenes](image-access-functions.md)
-   [Funciones de integridad de la imagen](image-integrity-functions.md)
-   [Funciones de modificación de imágenes](image-modification-functions.md)

 

 



