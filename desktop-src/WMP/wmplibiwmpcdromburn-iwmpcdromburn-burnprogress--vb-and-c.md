---
title: Propiedad IWMPCdromRomRom burnProgress
description: La propiedad burnProgress obtiene el progreso de la grabación de CD como porcentaje completado.
ms.assetid: 831cc55d-bd26-4328-a715-1a1fa48d7a40
keywords:
- propiedad burnProgress Reproductor de Windows Media
- La propiedad burnProgress Reproductor de Windows Media , interfaz IWMPCdromRomRom
- Interfaz IWMPCdromRom Reproductor de Windows Media , propiedad burnProgress
topic_type:
- apiref
api_name:
- IWMPCdromBurn.burnProgress
- IWMPCdromBurn.get_burnProgress
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90b8e468bc57bb40d990c0b2aeaffc23e184ef2ffa04ab85c9f60cf0d6bced57
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118332073"
---
# <a name="iwmpcdromburnburnprogress-property"></a>Propiedad IWMPCdromRom::burnProgress

La **propiedad burnProgress** obtiene el progreso de la grabación de CD como porcentaje completado.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```CSharp
public System.Int32 burnProgress {get;}
```


```VB

Public ReadOnly Property burnProgress As System.Int32
```





## <a name="property-value"></a>Valor de propiedad

**System.Int32 que** es el valor de progreso. Los valores de progreso van de 0 a 100.

## <a name="remarks"></a>Comentarios

El valor de progreso representa el porcentaje completado de todo el proceso de grabación, incluidas las operaciones de almacenamiento provisional.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Reproductor de Windows Media 11<br/>                                                                                     |
| Espacio de nombres<br/> | **WMPLib**<br/>                                                                                                  |
| Ensamblado<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Interfaz IWMPCdromRomRom (VB y C#)**](iwmpcdromburn--vb-and-c.md)
</dt> </dl>

 

 





