---
title: Método IDWriteTextLayout3 GetLineSpacing
description: Obtiene información de espaciado de línea.
ms.assetid: 6b93a3ec-c8ea-2e64-45b5-51565d6de173
keywords:
- Método GetLineSpacing de escritura directa
- Método GetLineSpacing direct write , interfaz IDWriteTextLayout3
- Método GetLineSpacing de la interfaz IDWriteTextLayout3
topic_type:
- apiref
api_name:
- IDWriteTextLayout3.GetLineSpacing
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 303030a5674f39c160804ae2dad5b91050d82f37
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160086"
---
# <a name="idwritetextlayout3getlinespacing-method"></a>Método IDWriteTextLayout3::GetLineSpacing

Obtiene información de espaciado de línea.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetLineSpacing(
  [out] DWRITE_LINE_SPACING *lineSpacingOptions
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lineSpacingOptions* \[ out\]
</dt> <dd>

Cómo administrar el espacio entre líneas.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
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

 

 





