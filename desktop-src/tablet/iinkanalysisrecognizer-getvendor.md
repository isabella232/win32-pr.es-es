---
description: Recupera el nombre del proveedor de IInkAnalysisRecognizer.
ms.assetid: 62ff209e-2a34-4c04-90a0-661d06898298
title: 'IInkAnalysisRecognizer:: GetVendor (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalysisRecognizer.GetVendor
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: a48bec62ed4a6a9d94d54ea3a1ba4a53eddd4b7b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154424"
---
# <a name="iinkanalysisrecognizergetvendor-method"></a>IInkAnalysisRecognizer:: GetVendor (método)

Recupera el nombre del proveedor de [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md).

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetVendor(
  [out] BSTR *pbstrVendor
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pbstrVendor* \[ enuncia\]
</dt> <dd>

Nombre del proveedor.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Observaciones

> [!Caution]  
> Para evitar una pérdida de memoria, llame a [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) en \* *pbstrVendor* cuando ya no necesite usar la cadena.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                     |
| Encabezado<br/>                   | <dl> <dt>IACom. h (también requiere IACom \_ i. c)</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md)
</dt> <dt>

[Referencia de análisis de tinta](ink-analysis-reference.md)
</dt> </dl>

 

