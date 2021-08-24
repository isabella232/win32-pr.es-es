---
description: Rutas de acceso curvadas
ms.assetid: 1ee9e6c6-5f8d-4727-b5f9-4b179c5371f1
title: Rutas de acceso curvadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b58018b7ef95b30c5ae2751ed963caefee7b9313ca86a8c6a2a4fee246908f8b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119849185"
---
# <a name="curved-paths"></a>Rutas de acceso curvadas

Una aplicación puede aplanar las curvas de un trazado llamando a la [**función FlattenPath.**](/windows/desktop/api/Wingdi/nf-wingdi-flattenpath) Esta función es especialmente útil para las aplicaciones que ajustan texto al contorno de un trazado que contiene curvas. Para ajustarse al texto, la aplicación debe realizar los pasos siguientes:

1.  Cree la ruta de acceso donde aparece el texto.
2.  Llame a [**la función FlattenPath**](/windows/desktop/api/Wingdi/nf-wingdi-flattenpath) para convertir las curvas de un trazado en segmentos de línea.
3.  Llame a [**la función GetPath**](/windows/desktop/api/Wingdi/nf-wingdi-getpath) para recuperar esos segmentos de línea.
4.  Calcule la longitud de cada línea y el ancho de cada carácter de la cadena.
5.  Use datos de ancho de línea y ancho de caracteres para colocar cada carácter a lo largo de la curva.

 

 



