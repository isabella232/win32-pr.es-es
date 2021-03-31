---
title: IDWriteTextLayout3 GetLineMetrics, método
description: Recupera las propiedades de cada línea.
ms.assetid: 352ca3e3-7b08-823c-0881-0b051d4ce574
keywords:
- Método GetLineMetrics de escritura directa
- Método GetLineMetrics de escritura directa, interfaz IDWriteTextLayout3
- Interfaz IDWriteTextLayout3 Direct Write, método GetLineMetrics
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491410"
---
# <a name="idwritetextlayout3getlinemetrics-method"></a>IDWriteTextLayout3:: GetLineMetrics (método)

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

*lineMetrics* \[ enuncia\]
</dt> <dd>

Matriz que se va a rellenar con información de línea.

</dd> <dt>

*maxLineCount* 
</dt> <dd>

Tamaño máximo de la matriz lineMetrics.

</dd> <dt>

*actualLineCount* \[ enuncia\]
</dt> <dd>

Tamaño real de la matriz de lineMetrics que se necesita.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="remarks"></a>Observaciones

Si maxLineCount no es suficientemente grande \_ y no hay suficiente \_ \_ búfer, que es equivalente a HRESULT \_ de \_ Win32 (error de \_ búfer insuficiente \_ ), se devuelve y actualLineCount se establece en el número de líneas necesarias.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio Windows 8.1\]<br/>                                            |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]<br/>                                 |
| Teléfono mínimo compatible<br/>  | Windows Phone 8,1 \[ Windows Phone aplicaciones de Windows Runtime Silverlight 8,1 y\]<br/> |
| Biblioteca<br/>                  | <dl> <dt>Dwrite. lib</dt> </dl>   |
| Archivo DLL<br/>                      | <dl> <dt>Dwrite.dll</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IDWriteTextLayout3**](idwritetextlayout3.md)
</dt> </dl>

 

 





