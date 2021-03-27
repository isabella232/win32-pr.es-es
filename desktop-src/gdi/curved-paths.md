---
description: Trazados curvos
ms.assetid: 1ee9e6c6-5f8d-4727-b5f9-4b179c5371f1
title: Trazados curvos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fe27e20d7c5c3f59ea4bd38b46049088ae9d409
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908503"
---
# <a name="curved-paths"></a>Trazados curvos

Una aplicación puede acoplar las curvas en un trazado mediante una llamada a la función [**FlattenPath**](/windows/desktop/api/Wingdi/nf-wingdi-flattenpath) . Esta función es especialmente útil para las aplicaciones que se ajustan al texto en el contorno de una ruta de acceso que contiene curvas. Para ajustar el texto, la aplicación debe realizar los siguientes pasos:

1.  Cree la ruta de acceso donde aparece el texto.
2.  Llame a la función [**FlattenPath**](/windows/desktop/api/Wingdi/nf-wingdi-flattenpath) para convertir las curvas de un trazado en segmentos de línea.
3.  Llame a la función [**GetPath**](/windows/desktop/api/Wingdi/nf-wingdi-getpath) para recuperar esos segmentos de línea.
4.  Calcular la longitud de cada línea y el ancho de cada carácter de la cadena.
5.  Use datos de ancho de línea y de ancho de caracteres para colocar cada carácter a lo largo de la curva.

 

 



