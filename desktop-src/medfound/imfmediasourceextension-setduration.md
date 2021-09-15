---
description: Establece la duración del origen multimedia en unidades de 100 nanosegundos.
ms.assetid: dc3dc600-ca81-40da-9edb-0af283ba9221
title: MÉTODO IMFMediaSourceExtension::SetDuration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaSourceExtension.SetDuration
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: ae669bf19f531034eacafac7fb89f3c07fa1e0e9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127474254"
---
# <a name="imfmediasourceextensionsetduration-method"></a>MÉTODO IMFMediaSourceExtension::SetDuration

Establece la duración del origen multimedia en unidades de 100 nanosegundos.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetDuration(
  [in] double duration
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*duración* \[ En\]
</dt> <dd>

Duración del origen multimedia en unidades de 100 nanosegundos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8.1 solo aplicaciones de escritorio\]<br/>                                                 |
| Servidor mínimo compatible<br/> | Windows Server 2012 Solo aplicaciones \[ de escritorio R2\]<br/>                                      |
| IDL<br/>                      | <dl> <dt>Mfmediaengine.idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**EXTENSIONMediaSourceExtension**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediasourceextension)
</dt> </dl>

 

 




