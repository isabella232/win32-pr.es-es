---
title: ITfContextRenderingMarkup GetRenderingMarkup, método
description: El método ITfContextRenderingMarkup GetRenderingMarkup recupera un enumerador de los marcas de representación para el intervalo especificado.
ms.assetid: fe060eab-8a6b-4eb7-9c7f-353b887657d8
keywords:
- Método GetRenderingMarkup marco de trabajo de servicios de texto
- Método GetRenderingMarkup marco de trabajo de servicios de texto, interfaz ITfContextRenderingMarkup
- ITfContextRenderingMarkup interface Text Services Framework, método GetRenderingMarkup
topic_type:
- apiref
api_name:
- ITfContextRenderingMarkup.GetRenderingMarkup
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1f3ccfb97af6a6657c33982359640a2a924cad2f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792567"
---
# <a name="itfcontextrenderingmarkupgetrenderingmarkup-method"></a>ITfContextRenderingMarkup:: GetRenderingMarkup (método)

El método **ITfContextRenderingMarkup:: GetRenderingMarkup** recupera un enumerador de los marcas de representación para el intervalo especificado.

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

*EC* \[ de\]
</dt> <dd>

\[en \] una cookie de edición de solo lectura para tener acceso al contexto.

</dd> <dt>

*dwFlags* \[ de\]
</dt> <dd>

\[in\]



| Value                                                                                                                                                                                         | Significado                                                                                      |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <span id="TF_GRM_INCLUDE_PROPERTY"></span><span id="tf_grm_include_property"></span><dl> <dt>**\_propiedad de \_ inclusión TF GRM \_**</dt> </dl> | Si este bit es 1, el enumerador incluirá la \_ propiedad del atributo prop de GUID \_ .<br/> |



 

</dd> <dt>

*pRangeCover* \[ de\]
</dt> <dd>

\[en \] un puntero a una interfaz [ITfRange](/windows/desktop/api/Msctf/nn-msctf-itfrange) del intervalo para enumerar los marcas de representación.

</dd> <dt>

*ppEnum* \[ enuncia\]
</dt> <dd>

\[\]un puntero para recuperar el puntero de la interfaz [IEnumTfRenderingMarkup](/windows/desktop/TSF/ienumtfrenderingmarkup) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Value                                                                                | Descripción                           |
|--------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl> | Método realizado correctamente.<br/> |



 

## <a name="remarks"></a>Observaciones

> [!Note]  
> Este método no está actualmente en los archivos de encabezado públicos. Para usar esta API, debe compilar MIDL en el [prototipo](prototypes.md).

 

 

