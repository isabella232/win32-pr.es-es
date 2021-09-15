---
title: IWMPCdromIntegración de la propiedad burnState
description: La propiedad burnState obtiene un valor de enumeración que indica el estado de grabación actual.
ms.assetid: 2bb543f9-9e4c-4425-99d6-ac89ef7f5807
keywords:
- propiedad burnState Reproductor de Windows Media
- Propiedad burnState Reproductor de Windows Media , interfaz IWMPCdromRomRom
- Interfaz IWMPCdromIntegración Reproductor de Windows Media , propiedad burnState
topic_type:
- apiref
api_name:
- IWMPCdromBurn.burnState
- IWMPCdromBurn.get_burnState
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c6b1aa8ec39f032e8f130a75370131bd2894c64
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127569032"
---
# <a name="iwmpcdromburnburnstate-property"></a>IWMPCdromIntegración::burnState, propiedad

La **propiedad burnState** obtiene un valor de enumeración que indica el estado de grabación actual.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```CSharp
public WMPBurnState burnState {get;}
```


```VB

Public ReadOnly Property burnState As WMPBurnState
```





## <a name="property-value"></a>Valor de propiedad

**WMPLib.WMPState que** es un valor de la enumeración **WMPState** que indica el estado actual.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Reproductor de Windows Media 11.<br/>                                                                                    |
| Espacio de nombres<br/> | **WMPLib**<br/>                                                                                                  |
| Ensamblado<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IWMPCdromRomRom (VB y C#)**](iwmpcdromburn--vb-and-c.md)
</dt> <dt>

[**WMPState**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpburnstate)
</dt> </dl>

 

 





