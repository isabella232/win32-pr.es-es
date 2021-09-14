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
ms.openlocfilehash: 343234fce2b93ac02255731a38025f6d7b9fac6f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127242979"
---
# <a name="iwmpclosedcaptioncaptioningid-property"></a>Propiedad IWMPClosedCaption::captioningId

La **propiedad IWMPClosedCaption** obtiene o establece el nombre del elemento HTML que muestra los subtítulos.

## <a name="syntax"></a>Sintaxis


```CSharp
public System.String captioningId {get; set;}
```


```VB

Public Property captioningId As System.String
```





## <a name="property-value"></a>Valor de propiedad

**System.String que** es el identificador del elemento HTML.

## <a name="remarks"></a>Observaciones

El nombre del elemento especificado puede ser cualquier elemento HTML de la página web, siempre que admita el **atributo innerHTML.** Si la página web contiene varios marcos, el nombre del elemento solo puede hacer referencia a un elemento en el mismo marco que el control Reproductor de Windows Media elemento.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
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

 

 





