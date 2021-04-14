---
description: Recupera un valor que indica si se ha establecido en este IContextNode el ConfirmationType pasado a este método.
ms.assetid: 4a96bc46-b627-4784-ad1d-1079f49592e5
title: 'IContextNode:: IsConfirmed (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.IsConfirmed
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 300e0126b4a1ff55d372ff31deebde0eab686645
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542051"
---
# <a name="icontextnodeisconfirmed-method"></a>IContextNode:: IsConfirmed (método)

Recupera un valor que indica si se ha establecido en este IContextNode el ConfirmationType pasado a este método.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT IsConfirmed(
  [in]  ConfirmationType confirmedType,
  [out] VARIANT_BOOL     *pfTypeConfirmed
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*confirmedType* \[ de\]
</dt> <dd>

El tipo de confirmación que se está probando.

</dd> <dt>

*pfTypeConfirmed* \[ enuncia\]
</dt> <dd>

**Variante \_ TRUE** si el tipo pasado en confirmedType se ha establecido en este objeto [**IContextNode**](icontextnode.md) ; de lo contrario, **Variant \_ false**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Observaciones

Este valor se establece mediante el método [**IContextNode:: CONFIRM**](icontextnode-confirm.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                     |
| Encabezado<br/>                   | <dl> <dt>IACom. h (también requiere IACom \_ i. c)</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IContextNode**](icontextnode.md)
</dt> <dt>

[**IContextNode:: CONFIRM**](icontextnode-confirm.md)
</dt> <dt>

[Referencia de análisis de tinta](ink-analysis-reference.md)
</dt> </dl>

 

 




