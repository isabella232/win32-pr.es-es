---
title: IDWriteColorGlyphRunEnumerator MoveNext (método)
description: Desplácese a la siguiente ejecución del glifo en el enumerador.
ms.assetid: E6336C0E-F880-485C-9111-A102298257C1
keywords:
- MoveNext (método) de escritura directa
- MoveNext Method Direct Write, IDWriteColorGlyphRunEnumerator (interfaz)
- Interfaz IDWriteColorGlyphRunEnumerator Direct Write, método MoveNext
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
ms.openlocfilehash: 15c9963916c07f1df8cf3cfedb49b9e3fd66d0df
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534498"
---
# <a name="idwritecolorglyphrunenumeratormovenext-method"></a>IDWriteColorGlyphRunEnumerator:: MoveNext (método)

Desplácese a la siguiente ejecución del glifo en el enumerador.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT MoveNext(
  [out] BOOL *haveRun
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*haveRun* \[ enuncia\]
</dt> <dd>

Tipo: **bool \** _

Devuelve _ *true** si hay una ejecución del siguiente glifo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Aplicaciones \[ para UWP de Windows 8.1 Desktop apps \|\]<br/>                                     |
| Servidor mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 R2 \|\]<br/>                          |
| Teléfono mínimo compatible<br/>  | Windows Phone 8,1 \[ Windows Phone aplicaciones de Windows Runtime Silverlight 8,1 y\]<br/> |
| Biblioteca<br/>                  | <dl> <dt>Dwrite. lib</dt> </dl>   |
| Archivo DLL<br/>                      | <dl> <dt>Dwrite.dll</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IDWriteColorGlyphRunEnumerator**](idwritecolorglyphrunenumerator.md)
</dt> </dl>

 

 





