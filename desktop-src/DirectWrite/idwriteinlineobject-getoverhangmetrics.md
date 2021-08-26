---
title: Método IDWriteInlineObject GetOvermetrics
description: IDWriteTextLayout llama a esta función de devolución de llamada para obtener las extensiones visibles (en DIP) del objeto en línea. En el caso de un mapa de bits simple, sin relleno y sin sobresalga, todos los sobresalciones serán simplemente ceros.
ms.assetid: b3b3e9f0-ee35-4117-9a62-a975c03b5ca9
keywords:
- Escritura directa del método GetOvermetrics
- Método GetOvermetrics direct write , interfaz IDWriteInlineObject
- IdWriteInlineObject interface Direct Write , GetOvermetrics method
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
ms.openlocfilehash: 011794fc3804435dd565a00035247436814c41474c60b66f90c5cb5d9594f6c7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119928155"
---
# <a name="idwriteinlineobjectgetoverhangmetrics-method"></a>Método IDWriteInlineObject::GetOvermetrics

[**IDWriteTextLayout llama**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) a esta función de devolución de llamada para obtener las extensiones visibles (en DIP) del objeto en línea. En el caso de un mapa de bits simple, sin relleno y sin sobresalga, todos los sobresalciones serán simplemente ceros.

Los sobresalciones deben devolverse en relación con el tamaño notificado del objeto (vea [**DWRITE \_ INLINE \_ OBJECT \_ METRICS**](/windows/win32/api/dwrite/ns-dwrite-dwrite_inline_object_metrics)) y no se deben ajustar en línea de base.

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

Tipo: **[ **DWRITE \_ OVER METRICS \_**](/windows/win32/api/dwrite/ns-dwrite-dwrite_overhang_metrics)\***

Sobreshoot de extensiones visibles (en DIP) fuera del objeto .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| Biblioteca<br/> | <dl> <dt>Dwrite.lib</dt> </dl> |
| Archivo DLL<br/>     | <dl> <dt>Dwrite.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IDWriteInlineObject**](/windows/win32/api/dwrite/nn-dwrite-idwriteinlineobject)
</dt> <dt>

[**IDWriteInlineObject**](/windows/win32/api/dwrite/nn-dwrite-idwriteinlineobject)
</dt> </dl>

 

