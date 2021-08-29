---
description: Recupera el nombre de proveedor del IInkAnalysisRecognizer.
ms.assetid: 62ff209e-2a34-4c04-90a0-661d06898298
title: Método IInkAnalysisRecognizer::GetVendor (IACom.h)
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
ms.openlocfilehash: 8a2c77ba4019a4c6653b44a5b00259204191c7c51f26dd358e4e0be947434649
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119660525"
---
# <a name="iinkanalysisrecognizergetvendor-method"></a>IInkAnalysisRecognizer::GetVendor (método)

Recupera el nombre de proveedor de [**IInkAnalysisRecognizer.**](iinkanalysisrecognizer.md)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetVendor(
  [out] BSTR *pbstrVendor
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pbstrVendor* \[ out\]
</dt> <dd>

Nombre del proveedor.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores [devueltos, vea Clases e interfaces: análisis de entrada de lápiz.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Comentarios

> [!Caution]  
> Para evitar una pérdida de memoria, llame [**a SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) en \* *pbstrVendor* cuando ya no necesite usar la cadena.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                                                 |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>IACom.h (también requiere IACom \_ i.c)</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md)
</dt> <dt>

[Referencia de análisis de entrada de lápiz](ink-analysis-reference.md)
</dt> </dl>

 

