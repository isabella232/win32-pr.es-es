---
title: Propiedad Error de IWMPMedia2
description: La propiedad Error obtiene una interfaz IWMPErrorItem si el elemento multimedia tiene una condición de error.
ms.assetid: 57dc8aef-5f22-43da-87bc-fdc0c8ebe49b
keywords:
- Propiedad error Reproductor de Windows Media
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
ms.openlocfilehash: 6c841e52f2a5adda5a2098f591b141aa334ee5138c1a5cc7d6eff9b54dca5e92
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118331984"
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

## <a name="remarks"></a>Comentarios

Si no se puede reproducir el elemento multimedia, esta propiedad obtiene una **interfaz IWMPErrorItem** que contiene información sobre el problema detectado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Reproductor de Windows Media serie 9 o posterior<br/>                                                                      |
| Espacio de nombres<br/> | **WMPLib**<br/>                                                                                                  |
| Ensamblado<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IWMPErrorItem (VB y C#)**](iwmperroritem--vb-and-c.md)
</dt> <dt>

[**Interfaz IWMPMedia2 (VB y C#)**](iwmpmedia2--vb-and-c.md)
</dt> </dl>

 

 





