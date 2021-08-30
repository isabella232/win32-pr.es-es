---
title: Método IDWriteTextFormat2 SetLineSpacing
description: Establezca el espaciado de línea. | Método IDWriteTextFormat2 SetLineSpacing
ms.assetid: 71d8c6c4-920f-a1b5-5a13-9985a7aca41e
keywords:
- SetLineSpacing method Direct Write
- Método SetLineSpacing Direct Write , interfaz IDWriteTextFormat2
- Método Direct Write de la interfaz IDWriteTextFormat2, SetLineSpacing
topic_type:
- apiref
api_name:
- IDWriteTextFormat2.SetLineSpacing
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4298d4671b6f1b9a5a46e4ffdeb450540c2a8eb7f547d1a8dd0f0c0768f54d84
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120075555"
---
# <a name="idwritetextformat2setlinespacing-method"></a>Método IDWriteTextFormat2::SetLineSpacing

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

Tipo: **const [**DWRITE \_ LINE \_ SPACING**](/windows/win32/api/Dwrite_3/ns-dwrite_3-dwrite_line_spacing) \***

Cómo administrar el espacio entre líneas.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8.1 solo aplicaciones de escritorio\]<br/>                                            |
| Servidor mínimo compatible<br/> | Windows Server 2012 Solo aplicaciones \[ de escritorio R2\]<br/>                                 |
| Teléfono mínimo compatible<br/>  | Windows Phone 8.1 \[ Windows Phone Silverlight 8.1 y Windows Runtime\]<br/> |
| Biblioteca<br/>                  | <dl> <dt>Dwrite.lib</dt> </dl>   |
| Archivo DLL<br/>                      | <dl> <dt>Dwrite.dll</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IDWriteTextFormat2**](idwritetextformat2.md)
</dt> </dl>

 

 





