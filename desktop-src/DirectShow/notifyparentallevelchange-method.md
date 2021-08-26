---
description: El método NotifyParentalLevelChange habilita o deshabilita el control de eventos para los comandos temporales de nivel de administración parental.
ms.assetid: c8252cc6-a83f-4cce-ba3e-7db669eeb465
title: Método NotifyParentalLevelChange (Segment.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8382b52f64d4196b0ef74e5f3285e9bb047a4e1f77d3b0e5bec4da218ee753b3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119997365"
---
# <a name="notifyparentallevelchange-method"></a>NotifyParentalLevelChange (método)

> [!Note]  
> Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003. En versiones posteriores podría modificarse o no estar disponible.

 

El `NotifyParentalLevelChange` método habilita o deshabilita el control de eventos para los comandos temporales de nivel de administración parental.

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

## <a name="remarks"></a>Comentarios

Las notificaciones de administración parental están deshabilitadas de forma predeterminada. Esto significa que se permiten los comandos parentales temporales del disco, pero se omiten y el disco se reproducirá sin interrupción. Llame a este método durante la inicialización de la aplicación si necesita controlar comandos temporales de nivel de administración parental desde el disco. Para deshabilitar la administración parental una vez habilitada, llame a este método con un argumento false. Para obtener más información sobre la administración parental, [**vea AcceptParentalLevelChange**](acceptparentallevelchange-method.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|--------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Segment.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SeleccioneParentalLevel.**](selectparentallevel-method.md)
</dt> <dt>

[**GetTitleParentalLevels**](gettitleparentallevels-method.md)
</dt> <dt>

[**GetPlayerParentalCountry**](getplayerparentalcountry-method.md)
</dt> <dt>

[**GetPlayerParentalLevel**](getplayerparentallevel-method.md)
</dt> <dt>

[**SeleccioneParentalCountry.**](selectparentalcountry-method.md)
</dt> </dl>

 

 




