---
title: Método IDWriteTextLayout3 SetLineSpacing
description: Establezca el espaciado de línea. | Método IDWriteTextLayout3 SetLineSpacing
ms.assetid: 1bfca257-189c-4d18-628c-aff8217d2775
keywords:
- SetLineSpacing method Direct Write
- Método SetLineSpacing Direct Write , interfaz IDWriteTextLayout3
- Interfaz IDWriteTextLayout3 Escritura directa, método SetLineSpacing
topic_type:
- apiref
api_name:
- IDWriteTextLayout3.SetLineSpacing
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d1c054fd63beb85303a7d163a16b55f07613b687085be53e22d814b0003c63c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118649383"
---
# <a name="idwritetextlayout3setlinespacing-method"></a>Método IDWriteTextLayout3::SetLineSpacing

Establezca el espaciado de línea.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetLineSpacing(
  [in] const DWRITE_LINE_SPACING *lineSpacingOptions
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lineSpacingOptions* \[ En\]
</dt> <dd>

Cómo administrar el espacio entre líneas.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8.1 solo aplicaciones de escritorio\]<br/>                                            |
| Servidor mínimo compatible<br/> | Windows Server 2012 Solo aplicaciones \[ de escritorio R2\]<br/>                                 |
| Teléfono mínimo compatible<br/>  | Windows Phone 8.1 \[ Windows Phone Silverlight 8.1 y Windows Runtime\]<br/> |
| Biblioteca<br/>                  | <dl> <dt>Dwrite.lib</dt> </dl>   |
| Archivo DLL<br/>                      | <dl> <dt>Dwrite.dll</dt> </dl>   |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IDWriteTextLayout3**](idwritetextlayout3.md)
</dt> </dl>

 

 





