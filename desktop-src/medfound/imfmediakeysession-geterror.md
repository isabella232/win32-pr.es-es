---
description: Obtiene el estado de error asociado a la sesión de clave multimedia.
ms.assetid: 4693b7d5-59ee-472f-83fc-1ecbcc165dac
title: MÉTODO IMFMediaKeySession::GetError
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaKeySession.GetError
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 4f0a42601698a9cd62dc6cb23ca9e69ac2cc8a49
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127580440"
---
# <a name="imfmediakeysessiongeterror-method"></a>MÉTODO IMFMediaKeySession::GetError

Obtiene el estado de error asociado a la sesión de clave multimedia.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetError(
   USHORT *code,
   DWORD  *systemCode
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*code* 
</dt> <dd>

Código de error.

</dd> <dt>

*systemCode* 
</dt> <dd>

Información de error específica de la plataforma.

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

[**IMFMediaKeySession**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediakeysession)
</dt> </dl>

 

 




