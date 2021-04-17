---
description: No se admite la función RKeyOpenKeyService.
ms.assetid: 3af18cf7-bc98-4ebc-a62c-7234e9fbddaa
title: Función RKeyOpenKeyService (Rkeysvcc. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RKeyOpenKeyService
api_type:
- HeaderDef
api_location:
- Rkeysvcc.h
ms.openlocfilehash: ce905594d1ed088eb72dc59a1fa6beec576384ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687909"
---
# <a name="rkeyopenkeyservice-function"></a>RKeyOpenKeyService función)

No se admite la función **RKeyOpenKeyService** .

**Windows Server 2003:** La función **RKeyOpenKeyService** establece una conexión a un equipo remoto y abre un identificador del servicio de claves. Posteriormente, la función [**RKeyPFXInstall**](rkeypfxinstall.md) puede usar el identificador del servicio de claves. Tenga en cuenta que este comportamiento ha cambiado con Windows Server 2003 con Service Pack 1 (SP1).

## <a name="syntax"></a>Sintaxis


```C++
ULONG RKeyOpenKeyService(
  _In_    LPSTR          pszMachineName,
  _In_    KEYSVC_TYPE    OwnerType,
  _In_    LPWSTR         pwszOwnerName,
  _In_    void           *pAuthentication,
  _Inout_ void           *pReserved,
  _Out_   KEYSVCC_HANDLE *phKeySvcCli
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pszMachineName* \[ de\]
</dt> <dd>

Puntero largo a una cadena terminada en null que representa el equipo en el que se abrirá el identificador del servicio de claves.

</dd> <dt>

*OwnerType* \[ de\]
</dt> <dd>

[**KEYSVC \_**](keysvc-type.md) Valor de tipo que representa el tipo de clave. El único valor admitido es **KeySvcMachine**.

</dd> <dt>

*pwszOwnerName* \[ de\]
</dt> <dd>

Reservado. Establezca este valor en **null**.

</dd> <dt>

*pAuthentication* \[ de\]
</dt> <dd>

Un puntero a un valor **void** que representa la configuración de autenticación. Este puntero puede apuntar a un valor de cero o el valor siguiente.



| Value                                                                                                                                                                                                                                                           | Significado                                                                                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span id="RKEYSVC_CONNECT_SECURE_ONLY"></span><span id="rkeysvc_connect_secure_only"></span><dl> <dt>**RKEYSVC \_ CONECTAR \_ \_ solo con seguridad**</dt><dt></dt> </dl> | El cliente requiere autenticación mutua. Si se especifica este valor, se producirá un error de reserva en NTLM.<br/> |



 

</dd> <dt>

*conservado* \[ in, out\]
</dt> <dd>

Reservado. Establezca este valor en **null**.

</dd> <dt>

*phKeySvcCli* \[ enuncia\]
</dt> <dd>

Un puntero a un [**\_ identificador de KEYSVCC**](keysvcc-handle.md) que recibe el identificador del servicio de claves abierto. Cuando haya terminado de usar el identificador, libere el recurso mediante una llamada a la función [**RKeyCloseKeyService**](rkeyclosekeyservice.md) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es S \_ OK.

Si se produce un error en la función, el valor devuelto es un **ULong** que indica el error.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                             |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Rkeysvcc. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**RKeyCloseKeyService**](rkeyclosekeyservice.md)
</dt> <dt>

[**RKeyPFXInstall**](rkeypfxinstall.md)
</dt> </dl>

 

 




