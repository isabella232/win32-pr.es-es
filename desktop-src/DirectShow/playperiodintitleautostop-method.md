---
description: El método PlayPeriodInTitleAutoStop inicia la reproducción a la hora especificada en el título especificado hasta la hora de detenerse especificada.
ms.assetid: 0c4df76d-3991-4a6c-a8e5-5fd713eeffc2
title: Método PlayPeriodInTitleAutoStop
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 93dbf0a5c157efcf4d22e7e5ba650bfdfebc57fe6a43d319e0be14958d732024
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119564065"
---
# <a name="playperiodintitleautostop-method"></a>Método PlayPeriodInTitleAutoStop

> [!Note]  
> Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003. En versiones posteriores podría modificarse o no estar disponible.

 

El `PlayPeriodInTitleAutoStop` método inicia la reproducción a la hora especificada en el título especificado hasta la hora de detenerse especificada.

``` syntax
MSWebDVD.PlayPeriodInTitleAutoStop(iTitle, sStartTime, sEndTime)
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="iTitle"></span><span id="ititle"></span><span id="ITITLE"></span>*iTitle*
</dt> <dd>

Especifica el título como entero.

</dd> <dt>

<span id="sStartTime"></span><span id="sstarttime"></span><span id="SSTARTTIME"></span>*sStartTime*
</dt> <dd>

Especifica la hora de inicio como una cadena en formato "hh:mm:ss:ff" (especificando horas, minutos, segundos, fotogramas).

</dd> <dt>

<span id="sEndTime"></span><span id="sendtime"></span><span id="SENDTIME"></span>*sEndTime*
</dt> <dd>

Especifica la hora de finalización como una cadena en formato "hh:mm:ss:ff".

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**PlayChaptersAutoStop**](playchaptersautostop-method.md)
</dt> </dl>

 

 



