---
description: El método Stop detiene la reproducción.
ms.assetid: e1ebfacc-4f33-4b4d-8e6c-1d1e1f0a22bd
title: STOP (método) (DirectShow)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c8cae45c7f076f2c4e90f1e7f50676bebbd3482
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002610"
---
# <a name="stop-method-directshow"></a>STOP (método) (DirectShow)

> [!Note]  
> Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003. En versiones posteriores podría modificarse o no estar disponible.

 

El `Stop` método detiene la reproducción.

``` syntax
MSWebDVD.Stop()
```

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Si [**EnableResetOnStop**](enableresetonstop-property.md) se establece en true, la llamada a `Stop` coloca el navegador de DVD, junto con el resto del gráfico de filtro, en un estado detenido, lo que significa que la próxima vez que el usuario presione el botón **reproducir** , la reproducción comenzará al principio del disco. Si **EnableResetOnStop** se establece en true, la reproducción se reanuda donde se quedó cuando el usuario emite el siguiente comando **Play** .

 

 



