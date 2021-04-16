---
title: Propiedad de etiqueta IWMPCdromBurn
description: La propiedad etiqueta obtiene la cadena de etiqueta del volumen del CD.
ms.assetid: 46e7741c-59c5-46d8-b9ca-09892d907cd7
keywords:
- propiedades de etiqueta Media Player de Windows
- propiedad etiqueta Media Player Windows, interfaz IWMPCdromBurn
- Interfaz IWMPCdromBurn Windows Media Player, propiedad label
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718828"
---
# <a name="iwmpcdromburnlabel-property"></a>IWMPCdromBurn:: Label (propiedad)

La propiedad *etiqueta* obtiene la cadena de etiqueta del volumen del CD.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```CSharp
public System.String label {get;}
```


```VB

Public ReadOnly Property label As System.String
```





## <a name="property-value"></a>Valor de propiedad

**System. String** que es la cadena de la etiqueta de volumen.

## <a name="remarks"></a>Observaciones

Debido a la forma en que se almacenan las etiquetas de CD, la etiqueta del CD puede ser menor que la longitud de la cadena de etiqueta de volumen especificada. Si la cadena es mayor que la longitud máxima de una etiqueta de CD, se truncará el texto.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Windows Media Player 11.<br/>                                                                                    |
| Espacio de nombres<br/> | **WMPLib**<br/>                                                                                                  |
| Ensamblado<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IWMPCdromBurn (VB y C#)**](iwmpcdromburn--vb-and-c.md)
</dt> </dl>

 

 





