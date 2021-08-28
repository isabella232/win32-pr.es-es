---
description: Comprueba si un generador debe estar asociado a una propiedad determinada.
ms.assetid: 8fab2dc2-3549-4559-b704-6783d929274e
title: IProvidePropertyBuilder::MapPropertyToBuilder (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IProvidePropertyBuilder.MapPropertyToBuilder
api_type:
- COM
api_location:
- Vsp.dll
ms.openlocfilehash: 35ff9e82164251c4490355bbf0499b7fa690415d388b95f7f9c7fd0e6bd7dd3c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120001695"
---
# <a name="iprovidepropertybuildermappropertytobuilder-method"></a>IProvidePropertyBuilder::MapPropertyToBuilder (método)

Comprueba si un generador debe estar asociado a una propiedad determinada.

## <a name="syntax"></a>Sintaxis


```C++
void MapPropertyToBuilder(
  [in]          LONG   dispid,
  [out]         DWORD  *pdwCtlBldType,
  [out]         LPBSTR pbstrGuidBldr,
  [out, retval] LPBOOL builderAvailable
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*despid* \[ En\]
</dt> <dd>

DISPID de la propiedad en cuestión.

</dd> <dt>

*pdwCtlBldType* \[ out\]
</dt> <dd>

Generador que se va a asignar. Este parámetro puede ser una combinación de los valores siguientes.



| Value                                                                                                                                                                                                                                                          | Significado                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <span id="CTLBLDTYPE_FSTDPROPBUILDER"></span><span id="ctlbldtype_fstdpropbuilder"></span><dl> <dt>**CTLBLDTYPE \_ FSTDPROPBUILDER**</dt> <dt>1</dt> </dl>    | Invoque un generador de sistemas estándar (no se admite en Visual Studio).<br/> |
| <span id="CTLBLDTYPE_FINTERNALBUILDER"></span><span id="ctlbldtype_finternalbuilder"></span><dl> <dt>**CTLBLDTYPE \_ FINTERNALBUILDER**</dt> <dt>2</dt> </dl> | Invoca un generador personalizado.<br/>                                           |
| <span id="CTLBLDTYPE_EDITSOBJDIRECTLY"></span><span id="ctlbldtype_editsobjdirectly"></span><dl> <dt>**CTLBLDTYPE \_ EDITSOBJDIRECTLY**</dt> <dt>4</dt> </dl> | El compilador modifica el objeto. Se trata de un comportamiento normal.<br/>              |



 

</dd> <dt>

*pbstrGuidBldr* \[ out\]
</dt> <dd>

GUID que identifica el generador de esta propiedad.

</dd> <dt>

*builderAvailable* \[ out, retval\]
</dt> <dd>

Este parámetro es **TRUE si** esta propiedad admite actualmente un generador.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------|------------------------------------------------------------------------------------|
| Archivo DLL<br/> | <dl> <dt>Vsp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IProvidePropertyBuilder**](iprovidepropertybuilder.md)
</dt> </dl>

 

 




