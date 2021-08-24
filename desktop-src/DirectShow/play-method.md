---
description: El método Play reproduce el título del DVD actual.
ms.assetid: fe9dc266-5b12-479d-85cb-50cc6bb9d580
title: Método Play (DirectShow)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97d4cea7dc53afc6a116ad052da9a4ca0d52c2e8687d99bde854d3f89fa60a9a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119633565"
---
# <a name="play-method-directshow"></a>Método Play (DirectShow)

> [!Note]  
> Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003. En versiones posteriores podría modificarse o no estar disponible.

 

El `Play` método reproduce el título del DVD actual.

``` syntax
MSWebDVD.Play()
```

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Si la reproducción está en pausa o detenida y [**EnableResetOnStop**](enableresetonstop-property.md) es true, la llamada a **Play** reanudará la reproducción a velocidad normal en la ubicación actual. Si se detiene la reproducción y **EnableResetOnStop** es false, la llamada a **Play** hará que el disco empiece a reproducirse al principio del primer título.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Reanudar**](resume-method.md)
</dt> </dl>

 

 



