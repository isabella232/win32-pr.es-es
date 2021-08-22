---
title: Método WSMan.SessionFlagSkipCNCheck (WSManDisp.h)
description: Devuelve el valor de la marca de autenticación WSManFlagSkipCNCheck para su uso en el parámetro flags de WSMan.CreateSession.
ms.assetid: 44884a9d-ec5f-4822-945d-2681d214a902
ms.tgt_platform: multiple
keywords:
- Método SessionFlagSkipCNCheck Windows Remote Management
- Método SessionFlagSkipCNCheck Windows remote management , objeto WSMan
- WSMan object Windows Remote Management , SessionFlagSkipCNCheck (método)
topic_type:
- apiref
api_name:
- WSMan.SessionFlagSkipCNCheck
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 339246d88dd7dc86e23b1a97442788fb969eb9de5a36f89c4ebadecd9f6e32ed
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119613485"
---
# <a name="wsmansessionflagskipcncheck-method"></a>Método WSMan.SessionFlagSkipCNCheck

El **método WSMan.SessionFlagSkipCNCheck** devuelve el valor de la marca de autenticación **WSManFlagSkipCNCheck** para su uso en el parámetro *flags* de [**WSMan.CreateSession**](wsman-createsession.md). Este método proporciona una sintaxis más eficaz para usar la constante para que los scripts no sean necesarios para establecer un valor constante. Para obtener más información sobre cómo llamar a este método, vea [Constantes de sesión](session-constants.md).

**WSManFlagSkipCNCheck es** una constante en la **\_ \_ enumeración WSManSessionFlags.** Para obtener más información, vea [**Constantes de autenticación**](authentication-constants.md).

## <a name="syntax"></a>Sintaxis


```VB
WSMan.SessionFlagSkipCNCheck( _
  ByRef flags _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*flags* \[ out\]
</dt> <dd>

Valor de la constante.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                 |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                           |
| Header<br/>                   | <dl> <dt>WSManDisp.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>WSManDisp.idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>WSManDisp.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**WSMan**](wsman.md)
</dt> <dt>

[**Sesión**](session.md)
</dt> </dl>

 

 





