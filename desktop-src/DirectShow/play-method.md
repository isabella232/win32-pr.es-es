---
description: El método Play reproduce el título del DVD actual.
ms.assetid: fe9dc266-5b12-479d-85cb-50cc6bb9d580
title: Método Play (DirectShow)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f62323c9c86be476a35977dadf554bbfca3bca91
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061008"
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

## <a name="remarks"></a>Observaciones

Si la reproducción está en pausa o detenida y [**EnableResetOnStop**](enableresetonstop-property.md) es true, la llamada a **Play** reanudará la reproducción a velocidad normal en la ubicación actual. Si se detiene la reproducción y **EnableResetOnStop** es false, la llamada a **Play** hará que el disco empiece a reproducirse al principio del primer título.

## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Reanudar**](resume-method.md)
</dt> </dl>

 

 



