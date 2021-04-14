---
description: En el ejemplo siguiente se muestra cómo una aplicación puede recuperar el color del pincel de DC actual mediante las funciones SetDCBrushColor y GetDCBrushColor.
ms.assetid: a1ef6c25-0d00-4175-8679-001ba165bd6d
title: Establecer y recuperar el valor de color del pincel de contexto de dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21c684bfd50fd92959e9b8f7eac5baf96c62fd0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997661"
---
# <a name="setting-and-retrieving-the-device-context-brush-color-value"></a>Establecer y recuperar el valor de color del pincel de contexto de dispositivo

En el ejemplo siguiente se muestra cómo una aplicación puede recuperar el color del pincel de DC actual mediante las funciones [**SetDCBrushColor**](/windows/desktop/api/Wingdi/nf-wingdi-setdcbrushcolor) y [**GetDCBrushColor**](/windows/desktop/api/WinGdi/nf-wingdi-getdcbrushcolor) .


```C++
SelectObject(hdc,GetStockObject(DC_BRUSH));
SetDCBrushColor(hdc, RGB(00,0xff;00);
PatBlt(0,0,200,200,PATCOPY)
SetDCBrushColor(hdc,RGB(00,00,0xff);
PatBlt(0,0,200,200,PATCOPY);
```



 

 



