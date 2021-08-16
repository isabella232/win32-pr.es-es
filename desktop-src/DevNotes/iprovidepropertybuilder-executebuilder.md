---
description: Notifica a un objeto que debe mostrar su generador para la propiedad especificada.
ms.assetid: 4d855aed-aaa1-4cc8-be9d-1175c254a813
title: IProvidePropertyBuilder::ExecuteBuilder (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IProvidePropertyBuilder.ExecuteBuilder
api_type:
- COM
api_location:
- Vsp.dll
ms.openlocfilehash: 9aef31629cac755d5689de929c02fbc8d9b816bf868a48bd59df3d08c911d9b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117827292"
---
# <a name="iprovidepropertybuilderexecutebuilder-method"></a>IProvidePropertyBuilder::ExecuteBuilder (método)

Notifica a un objeto que debe mostrar su generador para la propiedad especificada.

## <a name="syntax"></a>Sintaxis


```C++
void ExecuteBuilder(
  [in]          LONG      dispid,
  [in]          BSTR      bstrGuidBldr,
  [in]          IDispatch *pdispApp,
  [in]          LONG_PTR  hwndBldrOwner,
  [in, out]     LPVARIANT pvarValue,
  [out, retval] LPBOOL    pbActionCommitted
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*desaconsulte* \[ En\]
</dt> <dd>

DISPID de la propiedad para la que se muestra el generador.

</dd> <dt>

*bstrGuidBldr* \[ En\]
</dt> <dd>

BSTR **del** GUID del generador que se va a invocar. Se devuelve desde [**MapToPropertyBuilder.**](iprovidepropertybuilder-mappropertytobuilder.md)

</dd> <dt>

*pdispApp* \[ En\]
</dt> <dd>

Se establece en **NULL.**

</dd> <dt>

*hwndBldrOwner* \[ En\]
</dt> <dd>

Identificador de la ventana primaria del generador emergente.

</dd> <dt>

*pvarValue* \[ in, out\]
</dt> <dd>

El valor actual de la propiedad. El objeto puede modificar este valor y cambiar al nuevo valor si *pbActionCommitted* es **TRUE.**

</dd> <dt>

*pbActionCommitted* \[ out, retval\]
</dt> <dd>

Valor que indica si el generador realizó una acción en el objeto . Se puede usar cuando un usuario modifica algo y, a continuación, presiona Aceptar en el cuadro de diálogo del generador emergente.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|------------------------------------------------------------------------------------|
| Archivo DLL<br/> | <dl> <dt>Vsp.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IProvidePropertyBuilder**](iprovidepropertybuilder.md)
</dt> </dl>

 

 




