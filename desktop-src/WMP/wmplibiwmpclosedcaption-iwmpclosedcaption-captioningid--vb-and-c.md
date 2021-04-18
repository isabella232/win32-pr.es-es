---
title: Propiedad captioningId de IWMPClosedCaption
description: La propiedad IWMPClosedCaption obtiene o establece el nombre del elemento HTML que muestra los subtítulos.
ms.assetid: b09bb7c7-c3b6-4e0d-962f-24b06a04f6d1
keywords:
- propiedades de captioningId Media Player de Windows
- propiedad captioningId de Windows Media Player, interfaz IWMPClosedCaption
- Interfaz IWMPClosedCaption Windows Media Player, propiedad captioningId
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649910"
---
# <a name="iwmpclosedcaptioncaptioningid-property"></a>IWMPClosedCaption:: captioningId (propiedad)

La propiedad **IWMPClosedCaption** obtiene o establece el nombre del elemento HTML que muestra los subtítulos.

## <a name="syntax"></a>Sintaxis


```CSharp
public System.String captioningId {get; set;}
```


```VB

Public Property captioningId As System.String
```





## <a name="property-value"></a>Valor de propiedad

**System. String** que es el identificador del elemento HTML.

## <a name="remarks"></a>Observaciones

El nombre de elemento especificado puede ser cualquier elemento HTML de la página web siempre que admita el atributo **innerHTML** . Si la página web contiene varios marcos, el nombre del elemento solo puede hacer referencia a un elemento del mismo marco que el control Media Player de Windows.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Windows Media Player 9 series o posterior<br/>                                                                      |
| Espacio de nombres<br/> | **WMPLib**<br/>                                                                                                  |
| Ensamblado<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Agregar subtítulos a medios digitales**](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[**Interfaz IWMPClosedCaption (VB y C#)**](iwmpclosedcaption--vb-and-c.md)
</dt> <dt>

[**Interfaz IWMPClosedCaption2 (VB y C#)**](iwmpclosedcaption2--vb-and-c.md)
</dt> </dl>

 

 





