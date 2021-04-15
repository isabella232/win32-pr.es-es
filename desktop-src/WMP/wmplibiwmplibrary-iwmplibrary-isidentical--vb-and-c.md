---
title: IWMPLibrary isIdentical, método
description: El método isIdentical devuelve un valor que indica si el objeto proporcionado es igual que el actual.
ms.assetid: c4eebc46-6a5f-4f9a-8cd4-7421b156670c
keywords:
- método isIdentical de Windows Media Player
- método isIdentical Windows Media Player, interfaz IWMPLibrary
- Interfaz IWMPLibrary Windows Media Player, método isIdentical
topic_type:
- apiref
api_name:
- IWMPLibrary.isIdentical
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53071caa98b8f8e3ccb95e926969926cc68e7860
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105709175"
---
# <a name="iwmplibraryisidentical-method"></a>IWMPLibrary:: isIdentical (método)

El método **isIdentical** devuelve un valor que indica si el objeto proporcionado es igual que el actual.

## <a name="syntax"></a>Sintaxis


```CSharp
public System.Boolean isIdentical(
  IWMPLibrary pIWMPLibrary
);
```


```VB

Public Function isIdentical( _
  ByVal pIWMPLibrary As IWMPLibrary _
) As System.Boolean
Implements IWMPLibrary.isIdentical
```





## <a name="parameters"></a>Parámetros

<dl> <dt>

*pIWMPLibrary* \[ de\]
</dt> <dd>

Una interfaz **WMPLib. IWMPLibrary** que representa el objeto que se va a comparar con el actual.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

**System. Boolean** que es el resultado de la comparación. El valor **true** indica que los objetos son iguales.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Windows Media Player 11.<br/>                                                                                    |
| Espacio de nombres<br/> | **WMPLib**<br/>                                                                                                  |
| Ensamblado<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IWMPLibrary (VB y C#)**](iwmplibrary--vb-and-c.md)
</dt> </dl>

 

 





