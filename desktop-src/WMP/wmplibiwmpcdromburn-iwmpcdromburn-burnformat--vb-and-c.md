---
title: Propiedad IWMPCdromRomRom burnFormat
description: La propiedad burnFormat obtiene un valor que indica el tipo de CD que se va a grabar.
ms.assetid: f60fcbd2-5d34-46f3-a2e2-29dac2ecf689
keywords:
- propiedad burnFormat Reproductor de Windows Media
- Interfaz de propiedad burnFormat Reproductor de Windows Media , IWMPCdromRomRom
- Interfaz IWMPCdromRom Reproductor de Windows Media , propiedad burnFormat
topic_type:
- apiref
api_name:
- IWMPCdromBurn.burnFormat
- IWMPCdromBurn.get_burnFormat
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 93d5dc4ff27b3650ee37f16a7e90eb535ebe373401363f8c93bd16d09061b7a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120000552"
---
# <a name="iwmpcdromburnburnformat-property"></a>Propiedad IWMPCdromRomRom::burnFormat

La **propiedad burnFormat** obtiene un valor que indica el tipo de CD que se va a grabar.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```CSharp
public WMPBurnFormat burnFormat {get;}
```


```VB

Public ReadOnly Property burnFormat As WMPBurnFormat
```





## <a name="property-value"></a>Valor de propiedad

**WMPLib.WMPLayoutFormat que** es un valor de la enumeración **WMPFormat que** indica el tipo de CD que se va a grabar.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------|----------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Reproductor de Windows Media 11<br/>                                                                             |
| Espacio de nombres<br/> | **WMPLib**<br/>                                                                                          |
| Ensamblado<br/>  | <dl> <dt>Interop.WMPLib (Interop.WMPLib.dll)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IWMPCdromRomRom (VB y C#)**](iwmpcdromburn--vb-and-c.md)
</dt> <dt>

[**WMPFormat**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpburnformat)
</dt> </dl>

 

 





