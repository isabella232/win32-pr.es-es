---
description: El método play reproduce el título actual del DVD.
ms.assetid: fe9dc266-5b12-479d-85cb-50cc6bb9d580
title: Play (método) (DirectShow)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f62323c9c86be476a35977dadf554bbfca3bca91
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537125"
---
# <a name="play-method-directshow"></a>Play (método) (DirectShow)

> [!Note]  
> Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003. En versiones posteriores podría modificarse o no estar disponible.

 

El `Play` método reproduce el título actual del DVD.

``` syntax
MSWebDVD.Play()
```

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Si la reproducción está pausada o detenida y [**EnableResetOnStop**](enableresetonstop-property.md) es true, al llamar a **Play** se reanudará la reproducción a velocidad normal en la ubicación actual. Si se detiene la reproducción y **EnableResetOnStop** es false, la llamada a **Play** hará que el disco empiece a reproducirse al principio del primer título.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Reanudar**](resume-method.md)
</dt> </dl>

 

 



