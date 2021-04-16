---
title: Propiedad burnFormat de IWMPCdromBurn
description: La propiedad burnFormat obtiene un valor que indica el tipo de CD que se va a grabar.
ms.assetid: f60fcbd2-5d34-46f3-a2e2-29dac2ecf689
keywords:
- propiedades de burnFormat Media Player de Windows
- propiedad burnFormat de Windows Media Player, interfaz IWMPCdromBurn
- Interfaz IWMPCdromBurn Windows Media Player, propiedad burnFormat
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
ms.openlocfilehash: 17e379727376b1ce272a95cd77c688fa611b291a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718844"
---
# <a name="iwmpcdromburnburnformat-property"></a>IWMPCdromBurn:: burnFormat (propiedad)

La propiedad **burnFormat** obtiene un valor que indica el tipo de CD que se va a grabar.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```CSharp
public WMPBurnFormat burnFormat {get;}
```


```VB

Public ReadOnly Property burnFormat As WMPBurnFormat
```





## <a name="property-value"></a>Valor de propiedad

Un **WMPLib. WMPBurnFormat** que es un valor de la enumeración **WMPBurnFormat** que indica el tipo de CD que se va a grabar.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------|----------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Reproductor de Windows Media 11<br/>                                                                             |
| Espacio de nombres<br/> | **WMPLib**<br/>                                                                                          |
| Ensamblado<br/>  | <dl> <dt>Interop. WMPLib (Interop.WMPLib.dll)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IWMPCdromBurn (VB y C#)**](iwmpcdromburn--vb-and-c.md)
</dt> <dt>

[**WMPBurnFormat**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpburnformat)
</dt> </dl>

 

 





