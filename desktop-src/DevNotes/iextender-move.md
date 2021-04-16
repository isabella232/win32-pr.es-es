---
description: Mueve un control MDIForm, Form o.
ms.assetid: 963e6533-f571-4043-bdd8-2596df6b5b35
title: 'IExtender:: Move (método)'
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
ms.openlocfilehash: 2c7ed806629f0e5e1bb0cdee5c76910728fd651d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105650113"
---
# <a name="iextendermove-method"></a>IExtender:: Move (método)

Mueve un control MDIForm, Form o.

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

*izquierda* \[ de\]
</dt> <dd>

Borde izquierdo del formulario o control.

</dd> <dt>

*parte superior* \[ de\]
</dt> <dd>

Borde superior del formulario o control.

</dd> <dt>

*ancho* \[ de de\]
</dt> <dd>

Ancho del formulario o control.

</dd> <dt>

*alto* \[ de de\]
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

[**IExtender**](iextender.md)
</dt> </dl>

 

 




