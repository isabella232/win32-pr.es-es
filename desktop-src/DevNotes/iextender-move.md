---
description: Mueve un MDIForm, un formulario o un control.
ms.assetid: 963e6533-f571-4043-bdd8-2596df6b5b35
title: IEmoverse::Move (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IExtender.Move
api_type:
- COM
api_location:
- Ole2disp.dll
- Oleaut32.dll
ms.openlocfilehash: 13002457952490588fa9e9ad40e7f66e7d31465b74f9757a3193ccaed1e8bf7e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120002105"
---
# <a name="iextendermove-method"></a>IEmoverse::Move (método)

Mueve un MDIForm, un formulario o un control.

## <a name="syntax"></a>Sintaxis


```C++
void Move(
  [in] object left,
  [in] object top,
  [in] object width,
  [in] object height
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*left* \[ En\]
</dt> <dd>

Borde izquierdo del formulario o control.

</dd> <dt>

*top* \[ En\]
</dt> <dd>

Borde superior del formulario o control.

</dd> <dt>

*width* \[ En\]
</dt> <dd>

Ancho del formulario o control.

</dd> <dt>

*alto* \[ En\]
</dt> <dd>

Alto del formulario o control.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Archivo DLL<br/> | <dl> <dt>Ole2disp.dll; </dt> <dt>Oleaut32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IE archiving**](iextender.md)
</dt> </dl>

 

 




