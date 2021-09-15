---
title: Propiedad IWMPCdromRom BurnProgress
description: La propiedad burnProgress obtiene el progreso de la grabación de CD como porcentaje completado.
ms.assetid: 831cc55d-bd26-4328-a715-1a1fa48d7a40
keywords:
- propiedades burnProgress Reproductor de Windows Media
- Propiedad burnProgress Reproductor de Windows Media , interfaz IWMPCdromRomRom
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
ms.openlocfilehash: 835c8c1091941437c226427ddb3ef53e8c577b5d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127569037"
---
# <a name="iwmpcdromburnburnprogress-property"></a>Propiedad IWMPCdromRomRom::burnProgress

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

**System.Int32 que** es el valor de progreso. Los valores de progreso oscilan entre 0 y 100.

## <a name="remarks"></a>Observaciones

El valor de progreso representa el porcentaje completado de todo el proceso de grabación, incluidas las operaciones de almacenamiento provisional.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Reproductor de Windows Media 11<br/>                                                                                     |
| Espacio de nombres<br/> | **WMPLib**<br/>                                                                                                  |
| Ensamblado<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IWMPCdromRomRom (VB y C#)**](iwmpcdromburn--vb-and-c.md)
</dt> </dl>

 

 





