---
description: Una aplicación realiza pruebas de posicionamiento en regiones para determinar las coordenadas de la posición actual del cursor.
ms.assetid: 861a2558-0967-43f6-be3f-580992da05ff
title: Regiones de pruebas de impacto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5734ffb886bd2978d3ee0b49773d752d4abf43a4d98dc060f3dfaf2956e3084a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118760981"
---
# <a name="hit-testing-regions"></a>Regiones de pruebas de impacto

Una aplicación realiza pruebas de posicionamiento en regiones para determinar las coordenadas de la posición actual del cursor. A continuación, pasa estas coordenadas, así como un identificador que identifica la región a la [**función PtInRegion.**](/windows/desktop/api/Wingdi/nf-wingdi-ptinregion) Las coordenadas del cursor se pueden recuperar procesando los distintos mensajes del mouse, como [**WM \_ LBUTTONDOWN,**](../inputdev/wm-lbuttondown.md) [**WM \_ LBUTTONUP,**](../inputdev/wm-lbuttonup.md) [**WM \_ RBUTTONDOWN**](../inputdev/wm-rbuttondown.md) y [**WM \_ RBUTTONUP.**](../inputdev/wm-rbuttonup.md) El valor devuelto para PtInRegion indica si la posición del cursor está dentro de la región determinada.

 

 
