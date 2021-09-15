---
title: IWMPCdromRip ripProgress, propiedad
description: La propiedad ripProgress obtiene el progreso de la instalación de CD como porcentaje completado.
ms.assetid: 00d4f074-a16d-4c5f-930f-4411b90303f1
keywords:
- propiedad ripProgress Reproductor de Windows Media
- propiedad ripProgress Reproductor de Windows Media , interfaz IWMPCdromRip
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
ms.openlocfilehash: 113b9fc716698156aa4f7731a7b19888e0edf438
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127568993"
---
# <a name="iwmpcdromripripprogress-property"></a>Propiedad IWMPCdromRip::ripProgress

La **propiedad ripProgress** obtiene el progreso de la instalación de CD como porcentaje completado.

## <a name="syntax"></a>Sintaxis


```CSharp
public System.Int32 ripProgress {get; set;}
```


```VB

Public ReadOnly Property ripProgress As System.Int32
```





## <a name="property-value"></a>Valor de propiedad

**System.Int32 que** es el valor de progreso. Los valores de progreso oscilan entre 0 y 100.

## <a name="remarks"></a>Observaciones

El valor de progreso representa el porcentaje completado de todo el proceso de esión. Para determinar el progreso de una pista específica, use [IWMPMedia.getItemInfo](wmplibiwmpplaylist-iwmpplaylist-getiteminfo--vb-and-c.md) con **RipProgress** como nombre del atributo. Para obtener el índice de la pista que se está viendo actualmente, llame a IWMPPlaylist.getItemInfo con "CurrentRipTrackIndex" como nombre del atributo.

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

[**Resalte un CD**](ripping-a-cd.md)
</dt> </dl>

 

 





