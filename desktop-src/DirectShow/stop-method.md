---
description: El método Stop detiene la reproducción.
ms.assetid: e1ebfacc-4f33-4b4d-8e6c-1d1e1f0a22bd
title: Método Stop (DirectShow)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f9eb216c3ad5c98dd1722ff941131198cfe662d025b20c3f71fe9ea758e0a7c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120050115"
---
# <a name="stop-method-directshow"></a>Método Stop (DirectShow)

> [!Note]  
> Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003. En versiones posteriores podría modificarse o no estar disponible.

 

El `Stop` método detiene la reproducción.

``` syntax
MSWebDVD.Stop()
```

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Si [**EnableResetOnStop**](enableresetonstop-property.md) está establecido en true, la llamada a coloca el navegador de DVD, junto con el resto del gráfico de filtros, en un estado detenido, lo que significa que la próxima vez que el usuario presione el botón Reproducir, la reproducción se iniciará al principio del `Stop` disco.  Si **EnableResetOnStop** está establecido en true, la reproducción se reanuda cuando el usuario emite el siguiente **comando Play.**

 

 



