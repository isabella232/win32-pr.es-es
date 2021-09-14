---
title: Método IDWriteInlineObject GetOvergeoMetrics
description: IDWriteTextLayout llama a esta función de devolución de llamada para obtener las extensiones visibles (en DIP) del objeto en línea. En el caso de un mapa de bits simple, sin relleno y sin sobresalte, todos los sobresalciones serán simplemente ceros.
ms.assetid: b3b3e9f0-ee35-4117-9a62-a975c03b5ca9
keywords:
- Escritura directa del método GetOvermetrics
- Método GetOvermetrics direct write , interfaz IDWriteInlineObject
- IdWriteInlineObject interface Direct Write , Método GetOvermetrics
topic_type:
- apiref
api_name:
- IDWriteInlineObject.GetOverhangMetrics
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a0960f28394c5b55c3377136451a5c13748edc1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127169873"
---
# <a name="idwriteinlineobjectgetoverhangmetrics-method"></a>IdWriteInlineObject::GetOvermetrics (método)

[**IDWriteTextLayout llama**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) a esta función de devolución de llamada para obtener las extensiones visibles (en DIP) del objeto en línea. En el caso de un mapa de bits simple, sin relleno y sin sobresalte, todos los sobresalciones serán simplemente ceros.

Los sobresaltores deben devolverse en relación con el tamaño notificado del objeto (vea [**DWRITE \_ INLINE \_ OBJECT \_ METRICS**](/windows/win32/api/dwrite/ns-dwrite-dwrite_inline_object_metrics)) y no deben ajustarse a la línea de base.

## <a name="syntax"></a>Sintaxis


```C++
virtual HRESULT GetOverhangMetrics(
  [out] DWRITE_OVERHANG_METRICS *overhangs
) = 0;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*sobresalciones* \[ out\]
</dt> <dd>

Tipo: **[ **DWRITE \_ OVERHANG \_ METRICS**](/windows/win32/api/dwrite/ns-dwrite-dwrite_overhang_metrics)\***

Sobreshoot de extensiones visibles (en DIP) fuera del objeto .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Biblioteca<br/> | <dl> <dt>Dwrite.lib</dt> </dl> |
| Archivo DLL<br/>     | <dl> <dt>Dwrite.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IDWriteInlineObject**](/windows/win32/api/dwrite/nn-dwrite-idwriteinlineobject)
</dt> <dt>

[**IDWriteInlineObject**](/windows/win32/api/dwrite/nn-dwrite-idwriteinlineobject)
</dt> </dl>

 

