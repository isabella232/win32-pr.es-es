---
title: Propiedad de equilibrio de IWMPSettings
description: La propiedad saldo obtiene o establece el equilibrio estéreo actual.
ms.assetid: 6b9b6305-3bab-418d-a172-d47ca4dbaba5
keywords:
- equilibrar las ventanas de propiedades Media Player
- propiedad saldo de Windows Media Player, interfaz IWMPSettings
- Interfaz IWMPSettings Windows Media Player, propiedad balance
topic_type:
- apiref
api_name:
- IWMPSettings.balance
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2085f4074d0cd09f475fc031213e3a583747a86b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718879"
---
# <a name="iwmpsettingsbalance-property"></a>IWMPSettings:: balance (propiedad)

La propiedad **saldo** obtiene o establece el equilibrio estéreo actual.

## <a name="syntax"></a>Sintaxis


```CSharp
public System.Int32 balance {get; set;}
```


```VB

Public Property balance As System.Int32
```





## <a name="property-value"></a>Valor de propiedad

**System. Int32** que es el valor de equilibrio. Este valor puede oscilar entre 100 y 100. El valor predeterminado es cero.

## <a name="remarks"></a>Observaciones

El valor cero indica que el audio se reproduce en el mismo volumen en los canales izquierdo y derecho. Un valor de 100 indica que el audio se reproduce solo en el canal izquierdo. Un valor de 100 indica que el audio se reproduce solo en el canal derecho.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Windows Media Player 9 series o posterior.<br/>                                                                     |
| Espacio de nombres<br/> | **WMPLib**<br/>                                                                                                  |
| Ensamblado<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IWMPSettings (VB y C#)**](iwmpsettings--vb-and-c.md)
</dt> </dl>

 

 





