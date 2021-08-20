---
description: En el ejemplo siguiente se muestra cómo una aplicación puede recuperar el color de pincel de controlador de dominio actual mediante las funciones SetDCBrushColor y GetDCBrushColor.
ms.assetid: a1ef6c25-0d00-4175-8679-001ba165bd6d
title: Establecer y recuperar el valor de color del pincel de contexto del dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3d2f99f80305336af74a775b6f090c678ab60dcc6fed6fe29e62d03aea98001
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117698204"
---
# <a name="setting-and-retrieving-the-device-context-brush-color-value"></a>Establecer y recuperar el valor de color del pincel de contexto del dispositivo

En el ejemplo siguiente se muestra cómo una aplicación puede recuperar el color de pincel de controlador de dominio actual mediante las funciones [**SetDCBrushColor**](/windows/desktop/api/Wingdi/nf-wingdi-setdcbrushcolor) y [**GetDCBrushColor.**](/windows/desktop/api/WinGdi/nf-wingdi-getdcbrushcolor)


```C++
SelectObject(hdc,GetStockObject(DC_BRUSH));
SetDCBrushColor(hdc,RGB(00,0xff,00));
PatBlt(hdc,0,0,200,200,PATCOPY);
SetDCBrushColor(hdc,RGB(00,00,0xff));
PatBlt(hdc,0,0,200,200,PATCOPY);
```



 

 



