---
title: IWMPCdromRip ripProgress, propiedad
description: La propiedad ripProgress obtiene el progreso de la extracción de CD como porcentaje completado.
ms.assetid: 00d4f074-a16d-4c5f-930f-4411b90303f1
keywords:
- propiedad ripProgress Reproductor de Windows Media
- Propiedad ripProgress Reproductor de Windows Media , interfaz IWMPCdromRip
- Interfaz IWMPCdromRip Reproductor de Windows Media , propiedad ripProgress
topic_type:
- apiref
api_name:
- IWMPCdromRip.ripProgress
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea0d80a9eeed0246c48c142177bb4611c8666ca8b4f783d51f472dada2bbdbc5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119246755"
---
# <a name="iwmpcdromripripprogress-property"></a>Propiedad IWMPCdromRip::ripProgress

La **propiedad ripProgress** obtiene el progreso de la extracción de CD como porcentaje completado.

## <a name="syntax"></a>Sintaxis


```CSharp
public System.Int32 ripProgress {get; set;}
```


```VB

Public ReadOnly Property ripProgress As System.Int32
```





## <a name="property-value"></a>Valor de propiedad

**System.Int32 que** es el valor de progreso. Los valores de progreso van de 0 a 100.

## <a name="remarks"></a>Observaciones

El valor de progreso representa el porcentaje completado de todo el proceso de esión. Para determinar el progreso de una pista específica, use [IWMPMedia.getItemInfo](wmplibiwmpplaylist-iwmpplaylist-getiteminfo--vb-and-c.md) con **RipProgress** como nombre del atributo. Para obtener el índice de la pista que se está arrasando actualmente, llame a IWMPPlaylist.getItemInfo con "CurrentRipTrackIndex" como nombre del atributo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Reproductor de Windows Media 11.<br/>                                                                                    |
| Espacio de nombres<br/> | **WMPLib**<br/>                                                                                                  |
| Ensamblado<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IWMPCdromRip (VB y C#)**](iwmpcdromrip--vb-and-c.md)
</dt> <dt>

[**Arrasar un CD**](ripping-a-cd.md)
</dt> </dl>

 

 





