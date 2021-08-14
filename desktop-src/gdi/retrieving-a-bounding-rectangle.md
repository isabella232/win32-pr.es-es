---
description: Una aplicación recupera las dimensiones del rectángulo delimitador de una región llamando a la función GetRgnBox.
ms.assetid: 3851d0f4-33ec-44db-9cb8-c2afb03ffc25
title: Recuperar un rectángulo delimitador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9b7182d7c8f48fa8629855849710a601db9f93fd7e9180f9024d798b5ce2ebe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117886155"
---
# <a name="retrieving-a-bounding-rectangle"></a>Recuperar un rectángulo delimitador

Una aplicación recupera las dimensiones del rectángulo delimitador de una región llamando a la [**función GetRgnBox.**](/windows/desktop/api/Wingdi/nf-wingdi-getrgnbox) Si la región es rectangular, **GetRgnBox** devuelve las dimensiones de la región. Si la región es elíptica, la función devuelve las dimensiones del rectángulo más pequeño que se puede dibujar alrededor de la elipse. Los lados largos del rectángulo tienen la misma longitud que el eje principal de la elipse y los lados cortos del rectángulo tienen la misma longitud que el eje secundario de la elipse. Si la región es poligonal, **GetRgnBox** devuelve las dimensiones del rectángulo más pequeño que se puede dibujar alrededor de todo el polígono.

 

 



