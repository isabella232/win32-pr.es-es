---
title: IDWriteTextLayout2 GetMetrics, método
description: Recupera las métricas generales de la cadena con formato.
ms.assetid: EADCD83A-9FF5-44AB-8AB5-35FCB3A84889
keywords:
- Método GetMetrics de escritura directa
- Método GetMetrics de escritura directa, interfaz IDWriteTextLayout2
- Interfaz IDWriteTextLayout2 Direct Write, método GetMetrics
topic_type:
- apiref
api_name:
- IDWriteTextLayout2.GetMetrics
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e393dfabb632641125d915e85f275977b20f0326
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686046"
---
# <a name="idwritetextlayout2getmetrics-method"></a>IDWriteTextLayout2:: GetMetrics (método)

Recupera las métricas generales de la cadena con formato.

## <a name="syntax"></a>Sintaxis


```C++
virtual HRESULT GetMetrics(
  [out] DWRITE_TEXT_METRICS1 * textMetrics
) = 0;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

 *textMetrics* \[ enuncia\]
</dt> <dd>

Escriba: **[**DWRITE \_ Text \_ METRICS1**](/windows/win32/api/dwrite_2/ns-dwrite_2-dwrite_text_metrics1) \** _

Cuando este método realiza la devolución, contiene las distancias de texto y el contenido asociado medidos después de dar formato.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: _ *HRESULT**

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

[**IDWriteTextLayout2**](idwritetextlayout2.md)
</dt> </dl>

 

 





