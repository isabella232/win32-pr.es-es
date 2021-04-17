---
title: IDWriteInlineObject GetOverhangMetrics, método
description: IDWriteTextLayout llama a esta función de devolución de llamada para obtener las extensiones visibles (en DIP) del objeto insertado. En el caso de un mapa de bits simple, sin relleno y sin voladizo, todos los sobrebloqueos serán simplemente ceros.
ms.assetid: b3b3e9f0-ee35-4117-9a62-a975c03b5ca9
keywords:
- Método GetOverhangMetrics de escritura directa
- Método GetOverhangMetrics de escritura directa, interfaz IDWriteInlineObject
- Interfaz IDWriteInlineObject Direct Write, método GetOverhangMetrics
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671208"
---
# <a name="idwriteinlineobjectgetoverhangmetrics-method"></a>IDWriteInlineObject:: GetOverhangMetrics (método)

[**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) llama a esta función de devolución de llamada para obtener las extensiones visibles (en DIP) del objeto insertado. En el caso de un mapa de bits simple, sin relleno y sin voladizo, todos los sobrebloqueos serán simplemente ceros.

Los sobrebloqueos deben devolverse en relación con el tamaño del objeto indicado (vea [**DWRITE \_ en \_ línea \_ métricas de objeto**](/windows/win32/api/dwrite/ns-dwrite-dwrite_inline_object_metrics)) y no deben ajustarse a la línea base.

## <a name="syntax"></a>Sintaxis


```C++
virtual HRESULT GetOverhangMetrics(
  [out] DWRITE_OVERHANG_METRICS *overhangs
) = 0;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*sobrebloqueos* \[ enuncia\]
</dt> <dd>

Tipo: **[ **\_ \_ métricas salientes de DWRITE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_overhang_metrics)\***

Exceso de extensiones visibles (en DIP) fuera del objeto.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Biblioteca<br/> | <dl> <dt>Dwrite. lib</dt> </dl> |
| Archivo DLL<br/>     | <dl> <dt>Dwrite.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IDWriteInlineObject**](/windows/win32/api/dwrite/nn-dwrite-idwriteinlineobject)
</dt> <dt>

[**IDWriteInlineObject**](/windows/win32/api/dwrite/nn-dwrite-idwriteinlineobject)
</dt> </dl>

 

