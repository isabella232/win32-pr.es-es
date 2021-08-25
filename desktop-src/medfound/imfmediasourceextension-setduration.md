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
ms.openlocfilehash: caad66946514eec91d1cac1dc9745b0d07d1546e32c9548297f01e76b921c46f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120061215"
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

*duration* \[ En\]
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
| Idl<br/>                      | <dl> <dt>Mfmediaengine.idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMFMediaSourceExtension**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediasourceextension)
</dt> </dl>

 

 




