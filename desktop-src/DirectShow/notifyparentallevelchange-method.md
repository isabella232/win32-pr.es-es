---
description: El método NotifyParentalLevelChange habilita o deshabilita el control de eventos para los comandos del nivel de administración parental temporal.
ms.assetid: c8252cc6-a83f-4cce-ba3e-7db669eeb465
title: Método NotifyParentalLevelChange (Segment. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc47b7d78af8cfdd32aa63361411e769c375ddf1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690409"
---
# <a name="notifyparentallevelchange-method"></a>Método NotifyParentalLevelChange

> [!Note]  
> Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003. En versiones posteriores podría modificarse o no estar disponible.

 

El `NotifyParentalLevelChange` método habilita o deshabilita el control de eventos para los comandos del nivel de administración parental temporal.

``` syntax
MSWebDVD.NotifyParentalLevelChange(bNotify)
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="bNotify"></span><span id="bnotify"></span><span id="BNOTIFY"></span>*bNotify*
</dt> <dd>

Especifica un valor booleano que indica si se notifica o no a la aplicación cuando el objeto MSWebDVD encuentra segmentos de vídeo con una clasificación más restrictiva que la clasificación general del disco.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Las notificaciones de administración parental están deshabilitadas de forma predeterminada. Esto significa que se permiten los comandos parentales temporales del disco, pero se omiten y el disco se reproducirá sin interrupción. Llame a este método durante la inicialización de la aplicación si necesita controlar los comandos del nivel de administración parental temporal del disco. Para deshabilitar la administración parental una vez habilitada, llame a este método con un argumento de false. Para obtener más información sobre la administración parental, vea [**AcceptParentalLevelChange**](acceptparentallevelchange-method.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|--------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Segmento. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SelectParentalLevel**](selectparentallevel-method.md)
</dt> <dt>

[**GetTitleParentalLevels**](gettitleparentallevels-method.md)
</dt> <dt>

[**GetPlayerParentalCountry**](getplayerparentalcountry-method.md)
</dt> <dt>

[**GetPlayerParentalLevel**](getplayerparentallevel-method.md)
</dt> <dt>

[**SelectParentalCountry**](selectparentalcountry-method.md)
</dt> </dl>

 

 




