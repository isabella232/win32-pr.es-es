---
description: Indique que se ha alcanzado el final de la secuencia multimedia.
ms.assetid: 6d6bffcc-aa3c-4825-9268-00dcd2a347e6
title: MÉTODO IMFMediaSourceExtension::SetEndOfStream
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaSourceExtension.SetEndOfStream
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 9018d76ce13bf441ea98134eb751f9e472f6bca8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127580437"
---
# <a name="imfmediasourceextensionsetendofstream-method"></a>MÉTODO IMFMediaSourceExtension::SetEndOfStream

Indique que se ha alcanzado el final de la secuencia multimedia.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetEndOfStream(
  [in] MF_MSE_ERROR error
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*error* \[ En\]
</dt> <dd>

Se usa para pasar información de error.

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

[**IMFMediaSourceExtension**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediasourceextension)
</dt> <dt>

[**\_ERROR DE MSE DE MF \_**](mf-mse-error.md)
</dt> </dl>

 

 




