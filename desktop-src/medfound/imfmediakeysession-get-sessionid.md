---
description: Obtiene un identificador de sesión único creado para esta sesión.
ms.assetid: 779ebea9-69ff-469a-8ee0-06d570ede6cb
title: MÉTODO IMFMediaKeySession::get_SessionId
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaKeySession.get_SessionId
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: f598cbb1d7122bb8597d5849778a833462b4e6d9de48942fdfabbc95bbc30898
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119724555"
---
# <a name="imfmediakeysessionget_sessionid-method"></a>MÉTODO IMFMediaKeySession::get \_ SessionId

Obtiene un identificador de sesión único creado para esta sesión.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_SessionId(
   BSTR *sessionId
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*sessionId* 
</dt> <dd>

Identificador de sesión de la clave multimedia.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8.1 solo aplicaciones de escritorio\]<br/>                                                 |
| Servidor mínimo compatible<br/> | Windows Server 2012 Solo aplicaciones \[ de escritorio R2\]<br/>                                      |
| Idl<br/>                      | <dl> <dt>Mfmediaengine.idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMFMediaKeySession**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediakeysession)
</dt> </dl>

 

 




