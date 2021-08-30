---
title: Propiedad maxBandwidth de IWMPNetwork
description: La propiedad maxBandwidth obtiene o establece el ancho de banda máximo permitido.
ms.assetid: ff7548d8-b80f-4cb4-bdd6-86d585fef329
keywords:
- Propiedad maxBandwidth Reproductor de Windows Media
- Propiedad maxBandwidth Reproductor de Windows Media , interfaz IWMPNetwork
- Interfaz IWMPNetwork Reproductor de Windows Media , propiedad maxBandwidth
topic_type:
- apiref
api_name:
- IWMPNetwork.maxBandwidth
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2f41e296e63f6b6d98fd39134021c2f28097d595653590a82085f944aaf7910
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119999905"
---
# <a name="iwmpnetworkmaxbandwidth-property"></a>Propiedad IWMPNetwork::maxBandwidth

La **propiedad maxBandwidth** obtiene o establece el ancho de banda máximo permitido.

## <a name="syntax"></a>Syntax


```CSharp
public System.Int32 maxBandwidth {get; set;}
```


```VB

Public Property maxBandwidth As System.Int32
```





## <a name="property-value"></a>Valor de propiedad

**System.Int32 que** es el ancho de banda máximo.

## <a name="remarks"></a>Comentarios

Esta propiedad no tiene un valor predeterminado. El valor se puede especificar mientras Reproductor de Windows Media está reproduciendo, pero el cambio no tendrá efecto hasta que se libera el elemento multimedia actual abriendo otro o llamando a **AxWindowsMediaPlayer.close.** Reproductor de Windows Media intenta lograr el mayor ancho de banda posible. No se producirá ninguna reducción intencionada del ancho de banda a menos que se establezca este valor.

Esta configuración es útil para reducir la cantidad de ancho de banda utilizado, especialmente en el caso de una secuencia de velocidad de bits múltiple (MBR). Una secuencia MBR contiene varias secuencias con diferentes velocidades de bits. En algunos casos, puede ser conveniente usar una secuencia con una velocidad de bits inferior a la que requiere el cliente. En este caso, si se especifica una velocidad de bits inferior con la propiedad **IWMPNetwork.maxBandwidth,** se seleccionará una secuencia de velocidad de bits inferior. Por ejemplo, una secuencia MBR podría incluir secuencias codificadas a 20 kilobits por segundo (Kbps), 37 Kbps y 200 Kbps. El uso de **IWMPNetwork.maxBandwidth** para especificar una velocidad de bits de 50 000 (50 Kbps) seleccionará la secuencia de 37 Kbps en lugar de la secuencia de 200 Kbps.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Reproductor de Windows Media serie 9 o posterior<br/>                                                                      |
| Espacio de nombres<br/> | **WMPLib**<br/>                                                                                                  |
| Ensamblado<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**AxWindowsMediaPlayer.close (VB y C#)**](axwmplib-axwindowsmediaplayer-close.md)
</dt> <dt>

[**Interfaz IWMPNetwork (VB y C#)**](iwmpnetwork--vb-and-c.md)
</dt> </dl>

 

 





