---
title: Método MoveNext IDWriteColorGlyphRunEnumerator
description: Pase a la siguiente ejecución de glifo en el enumerador.
ms.assetid: E6336C0E-F880-485C-9111-A102298257C1
keywords:
- Escritura directa del método MoveNext
- Método MoveNext Direct Write , IDWriteColorGlyphRunEnumerator (interfaz)
- IdWriteColorGlyphRunEnumerator interface Direct Write , Método MoveNext
topic_type:
- apiref
api_name:
- IDWriteColorGlyphRunEnumerator.MoveNext
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee2764f8228f4ce6684d61bc8b40e9a3bded7abb723f7405cdbfa6e90035fbbe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119964105"
---
# <a name="idwritecolorglyphrunenumeratormovenext-method"></a>Método IDWriteColorGlyphRunEnumerator::MoveNext

Pase a la siguiente ejecución de glifo en el enumerador.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT MoveNext(
  [out] BOOL *haveRun
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*haveRun* \[ out\]
</dt> <dd>

Tipo: **BOOL \***

Devuelve **TRUE** si hay una siguiente ejecución de glifo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8.1 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Server 2012 Aplicaciones de \[ escritorio R2 \| aplicaciones para UWP\]<br/>                          |
| Teléfono mínimo compatible<br/>  | Windows Phone 8.1 \[ Windows Phone Silverlight 8.1 y Windows Runtime\]<br/> |
| Biblioteca<br/>                  | <dl> <dt>Dwrite.lib</dt> </dl>   |
| Archivo DLL<br/>                      | <dl> <dt>Dwrite.dll</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IDWriteColorGlyphRunEnumerator**](idwritecolorglyphrunenumerator.md)
</dt> </dl>

 

 





