---
title: Propiedad de volumen IWMPSettings
description: La propiedad volume obtiene o establece el volumen de reproducción actual.
ms.assetid: cff4fe70-9ca2-4419-bfc3-d622e8c72756
keywords:
- propiedad volume Reproductor de Windows Media
- propiedad volume Reproductor de Windows Media , interfaz IWMPSettings
- Interfaz IWMPSettings Reproductor de Windows Media , propiedad de volumen
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
ms.openlocfilehash: a2077547dd00b5c75b6ca77a966190db2bb3bb1bcde61d1f5c5b84c794af84e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118568402"
---
# <a name="iwmpsettingsvolume-property"></a>Propiedad IWMPSettings::volume

La **propiedad volume** obtiene o establece el volumen de reproducción actual.

## <a name="syntax"></a>Sintaxis


```CSharp
public System.Int32 volume {get; set;}
```


```VB

Public Property volume As System.Int32
```





## <a name="property-value"></a>Valor de propiedad

**System.Int32 que** es el nivel de volumen, que va de 0 a 100.

## <a name="remarks"></a>Observaciones

Un valor de cero no especifica ningún volumen (muted). Un valor de 100 especifica el volumen completo. Si no se especifica ningún valor para esta propiedad, el valor predeterminado es la última configuración de volumen establecida para Reproductor de Windows Media.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Reproductor de Windows Media serie 9 o posterior<br/>                                                                      |
| Espacio de nombres<br/> | **WMPLib**<br/>                                                                                                  |
| Ensamblado<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IWMPSettings (VB y C#)**](iwmpsettings--vb-and-c.md)
</dt> </dl>

 

 





