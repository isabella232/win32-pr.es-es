---
title: Propiedad IWMPClosedCaption captioningId
description: La propiedad IWMPClosedCaption obtiene o establece el nombre del elemento HTML que muestra los subtítulos.
ms.assetid: b09bb7c7-c3b6-4e0d-962f-24b06a04f6d1
keywords:
- propiedad captioningId Reproductor de Windows Media
- CaptioningId, propiedad Reproductor de Windows Media , interfaz IWMPClosedCaption
- Interfaz IWMPClosedCaption Reproductor de Windows Media , propiedad captioningId
topic_type:
- apiref
api_name:
- IWMPClosedCaption.captioningId
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45f6d4c10beb3f0fd94da0365d67b6c5ab480d36d5a3786021f538e9dcf4e90c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118116061"
---
# <a name="iwmpclosedcaptioncaptioningid-property"></a>Propiedad IWMPClosedCaption::captioningId

La **propiedad IWMPClosedCaption** obtiene o establece el nombre del elemento HTML que muestra los subtítulos.

## <a name="syntax"></a>Syntax


```CSharp
public System.String captioningId {get; set;}
```


```VB

Public Property captioningId As System.String
```





## <a name="property-value"></a>Valor de propiedad

**System.String que** es el identificador del elemento HTML.

## <a name="remarks"></a>Comentarios

El nombre del elemento especificado puede ser cualquier elemento HTML de la página web, siempre que admita el **atributo innerHTML.** Si la página web contiene varios fotogramas, el nombre del elemento solo puede hacer referencia a un elemento en el mismo marco que el control Reproductor de Windows Media elemento.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Reproductor de Windows Media serie 9 o posterior<br/>                                                                      |
| Espacio de nombres<br/> | **WMPLib**<br/>                                                                                                  |
| Ensamblado<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Adición de subtítulos a medios digitales**](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[**Interfaz IWMPClosedCaption (VB y C#)**](iwmpclosedcaption--vb-and-c.md)
</dt> <dt>

[**Interfaz IWMPClosedCaption2 (VB y C#)**](iwmpclosedcaption2--vb-and-c.md)
</dt> </dl>

 

 





