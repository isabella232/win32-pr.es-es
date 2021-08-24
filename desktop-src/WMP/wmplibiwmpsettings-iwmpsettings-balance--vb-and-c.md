---
title: Propiedad de saldo IWMPSettings
description: La propiedad balance obtiene o establece el saldo estéreo actual.
ms.assetid: 6b9b6305-3bab-418d-a172-d47ca4dbaba5
keywords:
- balance property Reproductor de Windows Media
- balance property Reproductor de Windows Media , IWMPSettings (interfaz)
- Interfaz IWMPSettings Reproductor de Windows Media , propiedad balance
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
ms.openlocfilehash: 76d519d656be6b4974e2b4dd2707aafb2bb153f6b26bafe75de948d5e50c67b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119861094"
---
# <a name="iwmpsettingsbalance-property"></a>Propiedad IWMPSettings::balance

La **propiedad balance** obtiene o establece el saldo estéreo actual.

## <a name="syntax"></a>Syntax


```CSharp
public System.Int32 balance {get; set;}
```


```VB

Public Property balance As System.Int32
```





## <a name="property-value"></a>Valor de propiedad

**System.Int32 que** es el valor de saldo. Este valor puede oscilar entre 100 y 100. El valor predeterminado es cero.

## <a name="remarks"></a>Comentarios

El valor cero indica que el audio se reproduce en el mismo volumen en los canales izquierdo y derecho. Un valor de 100 indica que el audio se reproduce solo en el canal izquierdo. Un valor de 100 indica que el audio se reproduce solo en el canal derecho.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Reproductor de Windows Media serie 9 o posterior.<br/>                                                                     |
| Espacio de nombres<br/> | **WMPLib**<br/>                                                                                                  |
| Ensamblado<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IWMPSettings (VB y C#)**](iwmpsettings--vb-and-c.md)
</dt> </dl>

 

 





