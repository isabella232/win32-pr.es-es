---
title: Método ITfContextRenderingMarkup GetRenderingMarkup
description: El método ITfContextRenderingMarkup GetRenderingMarkup recupera un enumerador de los marcados de representación para el intervalo especificado.
ms.assetid: fe060eab-8a6b-4eb7-9c7f-353b887657d8
keywords:
- Método GetRenderingMarkup Text Services Framework
- Método GetRenderingMarkup Text Services Framework interfaz , ITfContextRenderingMarkup
- Interfaz ITfContextRenderingMarkup Text Services Framework , método GetRenderingMarkup
topic_type:
- apiref
api_name:
- ITfContextRenderingMarkup.GetRenderingMarkup
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4a94c8a7cce8673560cf01091b819def343213bfde578df6ce1e8850e2721723
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119476964"
---
# <a name="itfcontextrenderingmarkupgetrenderingmarkup-method"></a>ITfContextRenderingMarkup::GetRenderingMarkup (método)

El **método ITfContextRenderingMarkup::GetRenderingMarkup** recupera un enumerador de los marcados de representación para el intervalo especificado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetRenderingMarkup(
  [in]  TfEditCookie           ec,
  [in]  DWORD                  dwFlags,
  [in]  ITfRange               *pRangeCover,
  [out] IEnumTfRenderingMarkup **ppEnum
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ec* \[ En\]
</dt> <dd>

\[en \] Una cookie de edición de solo lectura para acceder al contexto.

</dd> <dt>

*dwFlags* \[ En\]
</dt> <dd>

\[in\]



| Value                                                                                                                                                                                         | Significado                                                                                      |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <span id="TF_GRM_INCLUDE_PROPERTY"></span><span id="tf_grm_include_property"></span><dl> <dt>**TF \_ GRM \_ INCLUDE \_ PROPERTY**</dt> </dl> | Si este bit es 1, el enumerador incluirá la propiedad \_ GUID PROP \_ ATTRIBUTE.<br/> |



 

</dd> <dt>

*pRangeCover* \[ En\]
</dt> <dd>

\[en \] Puntero a una interfaz [ITfRange](/windows/desktop/api/Msctf/nn-msctf-itfrange) del intervalo para enumerar los marcados de representación.

</dd> <dt>

*ppEnum* \[ out\]
</dt> <dd>

\[out Puntero para recuperar el puntero de interfaz \] [IEnumTfRenderingMarkup.](/windows/desktop/TSF/ienumtfrenderingmarkup)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Value                                                                                | Descripción                           |
|--------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Método realizado correctamente.<br/> |



 

## <a name="remarks"></a>Observaciones

> [!Note]  
> Este método no está actualmente en los archivos de encabezado públicos. Para usar esta API, debe compilar midL en el [prototipo](prototypes.md).

 

 

