---
title: Propiedad Error de IWMPMedia2
description: La propiedad Error obtiene una interfaz IWMPErrorItem si el elemento multimedia tiene una condición de error.
ms.assetid: 57dc8aef-5f22-43da-87bc-fdc0c8ebe49b
keywords:
- Propiedades de error Reproductor de Windows Media
- Propiedad error Reproductor de Windows Media interfaz , IWMPMedia2
- Interfaz IWMPMedia2 Reproductor de Windows Media , propiedad Error
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127172722"
---
# <a name="iwmpmedia2error-property"></a>Propiedad IWMPMedia2::Error

La **propiedad Error** obtiene una interfaz **IWMPErrorItem** si el elemento multimedia tiene una condición de error.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```CSharp
public IWMPErrorItem Error {get;}
```


```VB

Public ReadOnly Property Error As IWMPErrorItem
```





## <a name="property-value"></a>Valor de propiedad

Interfaz **WMPLib.IWMPErrorItem** que proporciona acceso a información sobre la condición de error.

## <a name="remarks"></a>Observaciones

Si no se puede reproducir el elemento multimedia, esta propiedad obtiene una **interfaz IWMPErrorItem** que contiene información sobre el problema detectado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Reproductor de Windows Media serie 9 o posterior<br/>                                                                      |
| Espacio de nombres<br/> | **WMPLib**<br/>                                                                                                  |
| Ensamblado<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IWMPErrorItem (VB y C#)**](iwmperroritem--vb-and-c.md)
</dt> <dt>

[**Interfaz IWMPMedia2 (VB y C#)**](iwmpmedia2--vb-and-c.md)
</dt> </dl>

 

 





