---
title: Propiedad de volumen IWMPSettings
description: La propiedad de volumen obtiene o establece el volumen de reproducción actual.
ms.assetid: cff4fe70-9ca2-4419-bfc3-d622e8c72756
keywords:
- Media Player de propiedades de volumen de Windows
- propiedad de volumen Windows Media Player, interfaz IWMPSettings
- Interfaz IWMPSettings Windows Media Player, propiedad de volumen
topic_type:
- apiref
api_name:
- IWMPSettings.volume
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b21e50c9d3c52b7ce117d6c2ab681e592571c0f4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690154"
---
# <a name="iwmpsettingsvolume-property"></a>IWMPSettings:: Volume (propiedad)

La propiedad de **volumen** obtiene o establece el volumen de reproducción actual.

## <a name="syntax"></a>Sintaxis


```CSharp
public System.Int32 volume {get; set;}
```


```VB

Public Property volume As System.Int32
```





## <a name="property-value"></a>Valor de propiedad

**System. Int32** que es el nivel de volumen, comprendido entre 0 y 100.

## <a name="remarks"></a>Observaciones

Un valor de cero no especifica ningún volumen (silenciado). Un valor de 100 especifica el volumen completo. Si no se especifica ningún valor para esta propiedad, toma como valor predeterminado la última configuración de volumen establecida para Windows Media Player.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Windows Media Player 9 series o posterior<br/>                                                                      |
| Espacio de nombres<br/> | **WMPLib**<br/>                                                                                                  |
| Ensamblado<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IWMPSettings (VB y C#)**](iwmpsettings--vb-and-c.md)
</dt> </dl>

 

 





