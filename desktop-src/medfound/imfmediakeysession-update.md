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
ms.openlocfilehash: 15bc06523f0cf9a7dc433381dd596cea89608ce7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127474259"
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



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8.1 solo aplicaciones de escritorio\]<br/>                                                 |
| Servidor mínimo compatible<br/> | Windows Server 2012 Solo aplicaciones \[ de escritorio R2\]<br/>                                      |
| IDL<br/>                      | <dl> <dt>Mfmediaengine.idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMFMediaKeySession**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediakeysession)
</dt> </dl>

 

 




