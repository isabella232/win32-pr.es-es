---
title: Propiedad de etiqueta IWMPCdromRomRom
description: La propiedad label obtiene la cadena de etiqueta del volumen de CD.
ms.assetid: 46e7741c-59c5-46d8-b9ca-09892d907cd7
keywords:
- propiedad label Reproductor de Windows Media
- Propiedad label Reproductor de Windows Media , interfaz IWMPCdromRomRom
- IWMPCdromRom Interface Reproductor de Windows Media , propiedad de etiqueta
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
ms.openlocfilehash: d8b8917706e20b5d1361054ac5f6fd209c0026837c428ecba715727e3d828a4f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120000555"
---
# <a name="iwmpcdromburnlabel-property"></a>Propiedad IWMPCdromRomRom::label

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

## <a name="remarks"></a>Comentarios

Debido a la forma en que se almacenan las etiquetas de CD, la etiqueta del CD puede ser más corta que la longitud de la cadena de etiqueta de volumen especificada. Si la cadena es mayor que la longitud máxima de una etiqueta de CD, el texto se truncará.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Reproductor de Windows Media 11.<br/>                                                                                    |
| Espacio de nombres<br/> | **WMPLib**<br/>                                                                                                  |
| Ensamblado<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IWMPCdromRomRom (VB y C#)**](iwmpcdromburn--vb-and-c.md)
</dt> </dl>

 

 





