---
title: Propiedad de etiqueta IWMPCdrom Rpm
description: La propiedad label obtiene la cadena de etiqueta del volumen de CD.
ms.assetid: 46e7741c-59c5-46d8-b9ca-09892d907cd7
keywords:
- etiqueta de propiedad Reproductor de Windows Media
- propiedad label Reproductor de Windows Media , interfaz IWMPCdromRomRom
- Interfaz IWMPCdromRom Reproductor de Windows Media , propiedad label
topic_type:
- apiref
api_name:
- IWMPCdromBurn.label
- IWMPCdromBurn.get_label
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05da344f1148de7e79cb605135964c6ab8225ac0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127569013"
---
# <a name="iwmpcdromburnlabel-property"></a>Propiedad IWMPCdromRom::label

La *propiedad label* obtiene la cadena de etiqueta del volumen de CD.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```CSharp
public System.String label {get;}
```


```VB

Public ReadOnly Property label As System.String
```





## <a name="property-value"></a>Valor de propiedad

**System.String que** es la cadena de etiqueta de volumen.

## <a name="remarks"></a>Observaciones

Debido a la manera en que se almacenan las etiquetas de CD, la etiqueta del CD puede ser más corta que la longitud de la cadena de etiqueta de volumen especificada. Si la cadena es mayor que la longitud máxima de una etiqueta de CD, el texto se truncará.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Reproductor de Windows Media 11.<br/>                                                                                    |
| Espacio de nombres<br/> | **WMPLib**<br/>                                                                                                  |
| Ensamblado<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Interfaz IWMPCdromRomRom (VB y C#)**](iwmpcdromburn--vb-and-c.md)
</dt> </dl>

 

 





