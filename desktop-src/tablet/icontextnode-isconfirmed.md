---
description: Recupera un valor que indica si el valor confirmationType pasado a este método se ha establecido en este IContextNode.
ms.assetid: 4a96bc46-b627-4784-ad1d-1079f49592e5
title: Método IContextNode::IsConfirmed (IACom.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127262447"
---
# <a name="icontextnodeisconfirmed-method"></a>IContextNode::IsConfirmed (método)

Recupera un valor que indica si el valor confirmationType pasado a este método se ha establecido en este IContextNode.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT IsConfirmed(
  [in]  ConfirmationType confirmedType,
  [out] VARIANT_BOOL     *pfTypeConfirmed
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*confirmedType* \[ En\]
</dt> <dd>

Tipo de confirmación que se está probando.

</dd> <dt>

*pfTypeConfirmed* \[ out\]
</dt> <dd>

**VARIANT \_ TRUE** si el tipo pasado en confirmedType se ha establecido en este [**objeto IContextNode;**](icontextnode.md) en caso contrario, **VARIANT \_ FALSE**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores [devueltos, vea Clases e interfaces: análisis de entrada de lápiz.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Observaciones

El método [**IContextNode::Confirm**](icontextnode-confirm.md) establece este valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                                                 |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                     |
| Encabezado<br/>                   | <dl> <dt>IACom.h (también requiere IACom \_ i.c)</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IContextNode**](icontextnode.md)
</dt> <dt>

[**IContextNode::Confirm**](icontextnode-confirm.md)
</dt> <dt>

[Referencia de análisis de entrada de lápiz](ink-analysis-reference.md)
</dt> </dl>

 

 




