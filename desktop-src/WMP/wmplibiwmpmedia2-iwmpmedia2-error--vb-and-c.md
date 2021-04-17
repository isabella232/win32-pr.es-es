---
title: IWMPMedia2 (propiedad de error)
description: La propiedad error obtiene una interfaz IWMPErrorItem si el elemento multimedia tiene una condición de error.
ms.assetid: 57dc8aef-5f22-43da-87bc-fdc0c8ebe49b
keywords:
- Propiedad error de Windows Media Player
- Propiedad error de Windows Media Player, interfaz IWMPMedia2
- Interfaz IWMPMedia2 Windows Media Player, propiedad error
topic_type:
- apiref
api_name:
- IWMPMedia2.Error
- IWMPMedia2.get_Error
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2179b4604efd03574c78261575ce02311cd18a0c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670368"
---
# <a name="iwmpmedia2error-property"></a>IWMPMedia2:: error (propiedad)

La propiedad **error** obtiene una interfaz **IWMPErrorItem** si el elemento multimedia tiene una condición de error.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```CSharp
public IWMPErrorItem Error {get;}
```


```VB

Public ReadOnly Property Error As IWMPErrorItem
```





## <a name="property-value"></a>Valor de propiedad

Una interfaz **WMPLib. IWMPErrorItem** que proporciona acceso a información sobre la condición de error.

## <a name="remarks"></a>Observaciones

Si no se puede reproducir el elemento multimedia, esta propiedad obtiene una interfaz **IWMPErrorItem** que contiene información sobre el problema encontrado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Windows Media Player 9 series o posterior<br/>                                                                      |
| Espacio de nombres<br/> | **WMPLib**<br/>                                                                                                  |
| Ensamblado<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IWMPErrorItem (VB y C#)**](iwmperroritem--vb-and-c.md)
</dt> <dt>

[**Interfaz IWMPMedia2 (VB y C#)**](iwmpmedia2--vb-and-c.md)
</dt> </dl>

 

 





