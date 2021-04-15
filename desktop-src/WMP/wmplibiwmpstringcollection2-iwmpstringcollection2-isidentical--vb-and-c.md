---
title: IWMPStringCollection2 isIdentical, método
description: El método isIdentical devuelve un valor que indica si el objeto representado por la interfaz proporcionada es igual que el actual.
ms.assetid: 826e7fd8-88f8-4a2a-9ca0-82a500099272
keywords:
- método isIdentical de Windows Media Player
- método isIdentical Windows Media Player, interfaz IWMPStringCollection2
- Interfaz IWMPStringCollection2 Windows Media Player, método isIdentical
topic_type:
- apiref
api_name:
- IWMPStringCollection2.isIdentical
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2bb760dae213f28d44fbc707b4430cb151cfe578
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105709113"
---
# <a name="iwmpstringcollection2isidentical-method"></a>IWMPStringCollection2:: isIdentical (método)

El método **isIdentical** devuelve un valor que indica si el objeto representado por la interfaz proporcionada es igual que el actual.

## <a name="syntax"></a>Sintaxis


```CSharp
public System.Boolean isIdentical(
  IWMPStringCollection2 pIWMPStringCollection2
);
```


```VB

Public Function isIdentical( _
  ByVal pIWMPStringCollection2 As IWMPStringCollection2 _
) As System.Boolean
Implements IWMPStringCollection2.isIdentical
```





## <a name="parameters"></a>Parámetros

<dl> <dt>

*pIWMPStringCollection2* \[ de\]
</dt> <dd>

La interfaz **WMPLib. IWMPStringCollection2** que representa el objeto que se va a comparar con el actual.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

**System. Boolean** que es el resultado de la comparación. Un valor de **true** indica que los objetos de colección de cadenas son iguales.

## <a name="remarks"></a>Observaciones

Para usar este método, se requiere acceso de lectura a la biblioteca. Para obtener más información, vea [acceso a la biblioteca](library-access.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Windows Media Player 11.<br/>                                                                                    |
| Espacio de nombres<br/> | **WMPLib**<br/>                                                                                                  |
| Ensamblado<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IWMPStringCollection2 (VB y C#)**](iwmpstringcollection2--vb-and-c.md)
</dt> </dl>

 

 





