---
title: IWMPCdromBurn isAvailable (método)
description: El método isAvailable proporciona información acerca de la unidad de CD y el medio.
ms.assetid: 75e81f5f-5839-4012-b0b9-e77b3ca6f35c
keywords:
- isAvailable (método) Windows Media Player
- método isAvailable Windows Media Player, interfaz IWMPCdromBurn
- Interfaz IWMPCdromBurn Windows Media Player, isAvailable (método)
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718830"
---
# <a name="iwmpcdromburnisavailable-method"></a>IWMPCdromBurn:: isAvailable (método)

El método **isavailable** proporciona información acerca de la unidad de CD y el medio.

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

*bstrItem* \[ de\]
</dt> <dd>

**System. String** que contiene uno de los valores siguientes.



| Value | Descripción                 |
|-------|-----------------------------|
| Burn  | La unidad es una grabadora de CD.   |
| Disco  | Hay un CD en la unidad. |
| Borrar | El CD se puede borrar.       |
| Escritura | Se puede escribir en el CD.   |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

**System. Boolean** que indica el resultado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Windows Media Player 11.<br/>                                                                                    |
| Espacio de nombres<br/> | **WMPLib**<br/>                                                                                                  |
| Ensamblado<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IWMPCdromBurn (VB y C#)**](iwmpcdromburn--vb-and-c.md)
</dt> </dl>

 

 





