---
title: Propiedad maxBandwidth de IWMPNetwork
description: La propiedad maxBandwidth obtiene o establece el ancho de banda máximo permitido.
ms.assetid: ff7548d8-b80f-4cb4-bdd6-86d585fef329
keywords:
- propiedad maxBandwidth Media Player de Windows
- propiedad maxBandwidth Media Player de Windows, interfaz IWMPNetwork
- Interfaz IWMPNetwork Windows Media Player, propiedad maxBandwidth
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
ms.openlocfilehash: 3620d609db0f1786da673923f54d726b3c99994a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649937"
---
# <a name="iwmpnetworkmaxbandwidth-property"></a>IWMPNetwork:: maxBandwidth (propiedad)

La propiedad **maxBandwidth** obtiene o establece el ancho de banda máximo permitido.

## <a name="syntax"></a>Sintaxis


```CSharp
public System.Int32 maxBandwidth {get; set;}
```


```VB

Public Property maxBandwidth As System.Int32
```





## <a name="property-value"></a>Valor de propiedad

**System. Int32** que es el ancho de banda máximo.

## <a name="remarks"></a>Observaciones

Esta propiedad no tiene un valor predeterminado. El valor se puede especificar mientras se reproduce Windows Media Player, pero el cambio no surtirá efecto hasta que se libere el elemento multimedia actual; para ello, se abre otro o se llama a **AxWindowsMediaPlayer. Close**. Windows Media Player intenta lograr el ancho de banda más alto posible. No se producirá una reducción intencionada del ancho de banda a menos que se establezca este valor.

Esta configuración es útil para reducir la cantidad de ancho de banda que se usa, especialmente en el caso de una secuencia de velocidad de bits múltiple (MBR). Una secuencia MBR contiene varias secuencias con velocidades de bits diferentes. En algunos casos, puede ser conveniente usar una secuencia con una velocidad de bits menor que la que requiere el cliente. En este caso, si se especifica una velocidad de bits inferior con la propiedad **IWMPNetwork. maxBandwidth** , se seleccionará una secuencia de velocidad de bits inferior. Por ejemplo, una secuencia MBR podría incluir secuencias codificadas a 20 kilobits por segundo (kbps), 37 Kbps y 200 Kbps. El uso de **IWMPNetwork. maxBandwidth** para especificar una velocidad de bits de 50.000 (50 Kbps) seleccionará la secuencia de 37 kbps en lugar de la secuencia de 200 Kbps.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Windows Media Player 9 series o posterior<br/>                                                                      |
| Espacio de nombres<br/> | **WMPLib**<br/>                                                                                                  |
| Ensamblado<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**AxWindowsMediaPlayer. Close (VB y C#)**](axwmplib-axwindowsmediaplayer-close.md)
</dt> <dt>

[**Interfaz IWMPNetwork (VB y C#)**](iwmpnetwork--vb-and-c.md)
</dt> </dl>

 

 





