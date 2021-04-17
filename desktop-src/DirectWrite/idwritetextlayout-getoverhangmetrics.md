---
title: IDWriteTextLayout GetOverhangMetrics, método
description: Devuelve los sobrebloqueos (en DIP) del diseño y todos los objetos contenidos en él, incluidos los glifos de texto y los objetos insertados.
ms.assetid: 4b23f6c5-cacc-41e2-8934-6f95208b999a
keywords:
- Método GetOverhangMetrics de escritura directa
- Método GetOverhangMetrics de escritura directa, interfaz IDWriteTextLayout
- Interfaz IDWriteTextLayout Direct Write, método GetOverhangMetrics
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
ms.openlocfilehash: 8d8a015998f0a673a310319f93d8f4892dd4b1c4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670863"
---
# <a name="idwritetextlayoutgetoverhangmetrics-method"></a>IDWriteTextLayout:: GetOverhangMetrics (método)

Devuelve los sobrebloqueos (en DIP) del diseño y todos los objetos contenidos en él, incluidos los glifos de texto y los objetos insertados.

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

Excesos de extensiones visibles (en DIP) fuera del diseño.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="remarks"></a>Observaciones

Los subrayados y los tachados no contribuyen a la determinación del cuadro negro, ya que el representador los dibuja realmente, lo que puede dibujarlos en cualquier variedad de estilos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Biblioteca<br/> | <dl> <dt>Dwrite. lib</dt> </dl> |
| Archivo DLL<br/>     | <dl> <dt>Dwrite.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout)
</dt> <dt>

[**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout)
</dt> </dl>

 

