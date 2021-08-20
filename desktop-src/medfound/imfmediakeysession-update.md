---
description: Pasa un valor de clave con los datos asociados requeridos por el módulo de descifrado de contenido para el sistema de claves especificado.
ms.assetid: 29e66037-5f18-4724-b6f2-d85555e6af69
title: MÉTODO IMFMediaKeySession::Update
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaKeySession.Update
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 12c9877990ed9601ccf6b2911504b720088fa956dc76d6db9b97bac518db2d49
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118062984"
---
# <a name="imfmediakeysessionupdate-method"></a>MÉTODO IMFMediaKeySession::Update

Pasa un valor de clave con los datos asociados requeridos por el módulo de descifrado de contenido para el sistema de claves especificado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Update(
   const BYTE  *key,
         DWORD cb
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*key* 
</dt> <dd></dd> <dt>

*Cb* 
</dt> <dd>

Recuento en bytes de *la clave*.

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

 

 




