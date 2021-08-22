---
title: IWMPLibrary isIdentical (método)
description: El método isIdentical devuelve un valor que indica si el objeto proporcionado es el mismo que el actual.
ms.assetid: c4eebc46-6a5f-4f9a-8cd4-7421b156670c
keywords:
- Método isIdentical Reproductor de Windows Media
- Método isIdentical Reproductor de Windows Media , interfaz IWMPLibrary
- Interfaz IWMPLibrary Reproductor de Windows Media método , isIdentical
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
ms.openlocfilehash: d0ed37725bbda5b170ece8ce71c12499b42f0b361cbac3bbe65f1b875af06fc7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119506055"
---
# <a name="iwmplibraryisidentical-method"></a>IWMPLibrary::isIdentical (método)

El **método isIdentical** devuelve un valor que indica si el objeto proporcionado es el mismo que el actual.

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

*pIWMPLibrary* \[ En\]
</dt> <dd>

Interfaz **WMPLib.IWMPLibrary** que representa el objeto que se comparará con el actual.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

**System.Boolean** que es el resultado de la comparación. El valor **true** indica que los objetos son iguales.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Reproductor de Windows Media 11.<br/>                                                                                    |
| Espacio de nombres<br/> | **WMPLib**<br/>                                                                                                  |
| Ensamblado<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IWMPLibrary (VB y C#)**](iwmplibrary--vb-and-c.md)
</dt> </dl>

 

 





