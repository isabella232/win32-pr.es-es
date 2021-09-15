---
title: IWMPCdromRom IsAvailable (método)
description: El método isAvailable proporciona información sobre la unidad de CD y los medios.
ms.assetid: 75e81f5f-5839-4012-b0b9-e77b3ca6f35c
keywords:
- Método isAvailable Reproductor de Windows Media
- IsAvailable method Reproductor de Windows Media , IWMPCdromAsync (interfaz)
- Interfaz IWMPCdromAsync Reproductor de Windows Media método , isAvailable
topic_type:
- apiref
api_name:
- IWMPCdromBurn.isAvailable
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3d604cb9d9e170a3837fbd477db4c7ff309e1df
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127569016"
---
# <a name="iwmpcdromburnisavailable-method"></a>IWMPCdromAsync::isAvailable (Método)

El **método isAvailable** proporciona información sobre la unidad de CD y los medios.

## <a name="syntax"></a>Sintaxis


```CSharp
public System.Boolean isAvailable(
  System.String bstrItem
);
```


```VB

Public Function isAvailable( _
  ByVal bstrItem As System.String _
) As System.Boolean
Implements IWMPCdromBurn.isAvailable
```





## <a name="parameters"></a>Parámetros

<dl> <dt>

*bstrItem* \[ En\]
</dt> <dd>

**System.String que** contiene uno de los siguientes valores.



| Value | Descripción                 |
|-------|-----------------------------|
| Quemar  | La unidad es un cd- cd.   |
| Disco  | Hay un CD en la unidad. |
| Borrar | El CD se puede borrar.       |
| Escritura | Se puede escribir en el CD.   |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

**System.Boolean** que indica el resultado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Reproductor de Windows Media 11.<br/>                                                                                    |
| Espacio de nombres<br/> | **WMPLib**<br/>                                                                                                  |
| Ensamblado<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IWMPCdromRom (VB y C#)**](iwmpcdromburn--vb-and-c.md)
</dt> </dl>

 

 





