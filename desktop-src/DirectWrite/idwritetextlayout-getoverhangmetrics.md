---
title: Método IDWriteTextLayout GetOvergeoMetrics
description: Devuelve los sobresalciones (en DIP) del diseño y todos los objetos contenidos en él, incluidos los glifos de texto y los objetos en línea.
ms.assetid: 4b23f6c5-cacc-41e2-8934-6f95208b999a
keywords:
- Escritura directa del método GetOvermetrics
- Método GetOvermetrics Direct Write , interfaz IDWriteTextLayout
- Método Direct Write de la interfaz IDWriteTextLayout , GetOvermetrics
topic_type:
- apiref
api_name:
- IDWriteTextLayout.GetOverhangMetrics
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb3591df5dc02fdc63215ff2276202df62347ed21aef23991b4ddcadef094281
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118649750"
---
# <a name="idwritetextlayoutgetoverhangmetrics-method"></a>IdWriteTextLayout::GetOvermetrics (método)

Devuelve los sobresalciones (en DIP) del diseño y todos los objetos contenidos en él, incluidos los glifos de texto y los objetos en línea.

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

Sobreshoots de extensiones visibles (en DIP) fuera del diseño.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Observaciones

Los subrayados y los tachados no contribuyen a la determinación de la caja negra, ya que en realidad los dibuja el representador, que puede dibujarlos en cualquier variedad de estilos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Biblioteca<br/> | <dl> <dt>Dwrite.lib</dt> </dl> |
| Archivo DLL<br/>     | <dl> <dt>Dwrite.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout)
</dt> <dt>

[**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout)
</dt> </dl>

 

