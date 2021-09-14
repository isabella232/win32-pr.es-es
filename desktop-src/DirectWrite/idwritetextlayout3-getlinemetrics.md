---
title: Método IDWriteTextLayout3 GetLineMetrics
description: Recupera las propiedades de cada línea.
ms.assetid: 352ca3e3-7b08-823c-0881-0b051d4ce574
keywords:
- Escritura directa del método GetLineMetrics
- Método GetLineMetrics Direct Write , interfaz IDWriteTextLayout3
- IdWriteTextLayout3 interface Direct Write , Método GetLineMetrics
topic_type:
- apiref
api_name:
- IDWriteTextLayout3.GetLineMetrics
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d10a06cbf123b71e1308b45c747ac8a840a5fe1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160088"
---
# <a name="idwritetextlayout3getlinemetrics-method"></a>Método IDWriteTextLayout3::GetLineMetrics

Recupera las propiedades de cada línea.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetLineMetrics(
  [out] DWRITE_LINE_METRICS1 *lineMetrics,
        UINT32               maxLineCount,
  [out] UINT32               *actualLineCount
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lineMetrics* \[ out\]
</dt> <dd>

Matriz que se rellenará con información de línea.

</dd> <dt>

*maxLineCount* 
</dt> <dd>

Tamaño máximo de la matriz lineMetrics.

</dd> <dt>

*actualLineCount* \[ out\]
</dt> <dd>

Tamaño real de la matriz lineMetrics necesaria.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Observaciones

Si maxLineCount no es lo suficientemente grande como para E NOT SUFFICIENT BUFFER, que es equivalente a \_ \_ \_ HRESULT \_ FROM \_ WIN32(ERROR \_ INSUFFICIENT BUFFER), se devuelve y \_ realLineCount se establece en el número de líneas necesarias.

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

 

 





