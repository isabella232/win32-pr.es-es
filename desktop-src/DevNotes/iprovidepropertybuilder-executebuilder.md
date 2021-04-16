---
description: Notifica a un objeto que debe mostrar su generador para la propiedad especificada.
ms.assetid: 4d855aed-aaa1-4cc8-be9d-1175c254a813
title: 'IProvidePropertyBuilder:: ExecuteBuilder (método)'
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
ms.openlocfilehash: c37c2a4ca1003bd701ea141f1723f4ca16aa69c3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649567"
---
# <a name="iprovidepropertybuilderexecutebuilder-method"></a>IProvidePropertyBuilder:: ExecuteBuilder (método)

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

*DISPID* \[ de\]
</dt> <dd>

El DISPID de la propiedad que muestra el generador.

</dd> <dt>

*bstrGuidBldr* \[ de\]
</dt> <dd>

**BSTR** del GUID del compilador que se va a invocar. Se devuelve desde [**MapToPropertyBuilder**](iprovidepropertybuilder-mappropertytobuilder.md).

</dd> <dt>

*pdispApp* \[ de\]
</dt> <dd>

Se establece en **null**.

</dd> <dt>

*hwndBldrOwner* \[ de\]
</dt> <dd>

Identificador de la ventana primaria del generador emergente.

</dd> <dt>

*pvarValue* \[ in, out\]
</dt> <dd>

El valor actual de la propiedad. Este valor puede ser modificado por el objeto y cambia al nuevo valor si *pbActionCommitted* es **true**.

</dd> <dt>

*pbActionCommitted* \[ out, retval\]
</dt> <dd>

Valor que indica si el generador realizó una acción en el objeto. Se puede usar cuando un usuario modifica algo y, a continuación, presiona aceptar en el cuadro de diálogo Generador emergente.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor **HRESULT** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------|------------------------------------------------------------------------------------|
| Archivo DLL<br/> | <dl> <dt>Vsp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IProvidePropertyBuilder**](iprovidepropertybuilder.md)
</dt> </dl>

 

 




