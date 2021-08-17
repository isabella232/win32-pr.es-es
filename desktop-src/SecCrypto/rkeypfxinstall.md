---
description: No se admite la función RKeyPFXInstall.
ms.assetid: 061e3d9d-fc92-4204-92f3-f3425afdbe27
title: Función RKeyPFXInstall (Rkeysvcc.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RKeyPFXInstall
api_type:
- HeaderDef
api_location:
- Rkeysvcc.h
ms.openlocfilehash: f19a01e9132bf9c4b1e281a75b0e0d7a27b4f9c7f299eefdd47bef8d60daea97
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118900550"
---
# <a name="rkeypfxinstall-function"></a>Función RKeyPFXInstall

No **se admite la función RKeyPFXInstall.**

**Windows Server 2003:** La **función RKeyPFXInstall** instala un certificado en un equipo remoto. Tenga en cuenta que este comportamiento ha cambiado con Windows Server 2003 con Service Pack 1 (SP1).

## <a name="syntax"></a>Sintaxis


```C++
ULONG RKeyPFXInstall(
  _In_ KEYSVCC_HANDLE         hKeySvcCli,
  _In_ PKEYSVC_BLOB           pPFX,
  _In_ PKEYSVC_UNICODE_STRING pPassword,
  _In_ ULONG                  ulFlags
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hKeySvcCli* \[ En\]
</dt> <dd>

Identificador [**KEYSVCC \_ HANDLE**](keysvcc-handle.md) abierto previamente [**por RKeyOpenKeyService**](rkeyopenkeyservice.md). El identificador representa el equipo remoto que recibirá el certificado. Este valor no puede ser **NULL.**

</dd> <dt>

*pPFX* \[ En\]
</dt> <dd>

Puntero a una estructura [**KEYSVC \_ BLOB**](keysvc-blob.md) que representa el certificado que se debe instalar. El BLOB está en [*formato PKCS \# 12.*](../secgloss/p-gly.md)

</dd> <dt>

*pPassword* \[ En\]
</dt> <dd>

Puntero a una estructura [**DE \_ CADENA UNICODE \_ KEYSVC**](keysvc-unicode-string.md) que representa la contraseña del BLOB. Cuando haya terminado de usar la contraseña, borre la contraseña de la memoria mediante una llamada a la [**función SecureZeroMemory.**](/previous-versions/windows/desktop/legacy/aa366877(v=vs.85)) Para obtener más información sobre la protección de contraseñas, vea [Control de contraseñas.](../secbp/handling-passwords.md)

</dd> <dt>

*ulFlags* \[ En\]
</dt> <dd>

Marcas que especifican las opciones de instalación del certificado. Este parámetro puede ser cero o una combinación de los valores siguientes.



| Valor                                                                                                                                                                                                                                     | Significado                                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <span id="CRYPT_EXPORTABLE"></span><span id="crypt_exportable"></span><dl> <dt>**CRYPT \_ EXPORTABLE**</dt><dt></dt> </dl>              | Las claves importadas se marcan como exportables.<br/>                                           |
| <span id="CRYPT_MACHINE_KEYSET"></span><span id="crypt_machine_keyset"></span><dl> <dt>**CRYPT \_ CONJUNTO \_ DE CLAVES DE LA MÁQUINA**</dt><dt></dt> </dl> | Las claves privadas se almacenan en el equipo remoto y no en el usuario actual.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es S \_ OK.

Si se produce un error en la función, el valor devuelto es **un ULONG** que indica el error.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                             |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Rkeysvcc.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**RKeyCloseKeyService**](rkeyclosekeyservice.md)
</dt> <dt>

[**RKeyOpenKeyService**](rkeyopenkeyservice.md)
</dt> </dl>

 

 
