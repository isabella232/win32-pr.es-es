---
description: El método PlayPeriodInTitleAutoStop inicia la reproducción a la hora especificada en el título especificado hasta la hora de detención especificada.
ms.assetid: 0c4df76d-3991-4a6c-a8e5-5fd713eeffc2
title: Método PlayPeriodInTitleAutoStop
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d05899b66b7f1a11f8f5b177d311b9634a52595b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103906530"
---
# <a name="playperiodintitleautostop-method"></a>Método PlayPeriodInTitleAutoStop

> [!Note]  
> Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003. En versiones posteriores podría modificarse o no estar disponible.

 

El `PlayPeriodInTitleAutoStop` método inicia la reproducción a la hora especificada en el título especificado hasta la hora de detención especificada.

``` syntax
MSWebDVD.PlayPeriodInTitleAutoStop(iTitle, sStartTime, sEndTime)
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="iTitle"></span><span id="ititle"></span><span id="ITITLE"></span>*iTitle*
</dt> <dd>

Especifica el título como un entero.

</dd> <dt>

<span id="sStartTime"></span><span id="sstarttime"></span><span id="SSTARTTIME"></span>*sStartTime*
</dt> <dd>

Especifica la hora de inicio como una cadena en el formato "HH: mm: SS: FF" (especificando horas, minutos, segundos, fotogramas).

</dd> <dt>

<span id="sEndTime"></span><span id="sendtime"></span><span id="SENDTIME"></span>*sEndTime*
</dt> <dd>

Especifica la hora de finalización como una cadena con el formato "HH: mm: SS: FF".

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**PlayChaptersAutoStop**](playchaptersautostop-method.md)
</dt> </dl>

 

 



