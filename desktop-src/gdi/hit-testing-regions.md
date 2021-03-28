---
description: Una aplicación realiza pruebas de posicionamiento en regiones para determinar las coordenadas de la posición actual del cursor.
ms.assetid: 861a2558-0967-43f6-be3f-580992da05ff
title: Regiones de pruebas de posicionamiento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe136c3ba9ab4babfc1150ae4c3eee878cb42327
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276003"
---
# <a name="hit-testing-regions"></a>Regiones de pruebas de posicionamiento

Una aplicación realiza pruebas de posicionamiento en regiones para determinar las coordenadas de la posición actual del cursor. Después, pasa estas coordenadas, así como un identificador que identifica la región en la función [**PtInRegion**](/windows/desktop/api/Wingdi/nf-wingdi-ptinregion) . Las coordenadas del cursor se pueden recuperar procesando los diversos mensajes del mouse, [**como \_ WM LBUTTONDOWN**](../inputdev/wm-lbuttondown.md) , [**WM \_ LBUTTONUP**](../inputdev/wm-lbuttonup.md) , [**WM \_ RBUTTONDOWN**](../inputdev/wm-rbuttondown.md) y [**WM \_ RBUTTONUP**](../inputdev/wm-rbuttonup.md). El valor devuelto para PtInRegion indica si la posición del cursor está dentro de la región especificada.

 

 
