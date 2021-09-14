---
description: Crea un objeto de sesión de clave multimedia utilizando los datos de inicialización y los datos personalizados especificados. .
ms.assetid: 9f11433c-7cff-4a59-9d4a-7f4b56ba62cf
title: MÉTODO IMFMediaKeys::CreateSession
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaKeys.CreateSession
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 89d3abce0c1c15d472f7008fa0ef2c5f27bba6ad
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127263388"
---
# <a name="imfmediakeyscreatesession-method"></a>MÉTODO IMFMediaKeys::CreateSession

Crea un objeto de sesión de clave multimedia utilizando los datos de inicialización y los datos personalizados especificados. .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT CreateSession(
         BSTR                     mimeType,
   const BYTE                     *initData,
         DWORD                    cb,
   const BYTE                     *customData,
         DWORD                    cbCustomData,
         IMFMediaKeySessionNotify *notify,
         IMFMediaKeySession       **ppSession
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*mimeType* 
</dt> <dd>

Tipo MIME del contenedor multimedia utilizado para el contenido.

</dd> <dt>

*initData* 
</dt> <dd>

Datos de inicialización del sistema de claves.

</dd> <dt>

*Cb* 
</dt> <dd>

Recuento en bytes de *initData.*

</dd> <dt>

*customData* 
</dt> <dd>

Datos personalizados enviados al sistema de claves.

</dd> <dt>

*cbCustomData* 
</dt> <dd>

Recuento en bytes de *cbCustomData.*

</dd> <dt>

*Notificar* 
</dt> <dd>

Notificar

</dd> <dt>

*ppSession* 
</dt> <dd>

Sesión de clave multimedia.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8.1 solo aplicaciones de escritorio\]<br/>                                                 |
| Servidor mínimo compatible<br/> | Windows Server 2012 Solo aplicaciones \[ de escritorio R2\]<br/>                                      |
| IDL<br/>                      | <dl> <dt>Mfmediaengine.idl</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IMFMediaKeys**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediakeys)
</dt> </dl>

 

 




