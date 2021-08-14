---
title: Método WSMan.SessionFlagUseNoAuthentication (WSManDisp.h)
description: Devuelve el valor de la marca de autenticación WSManFlagUseNoAuthentication para su uso en el parámetro flags del método WSMan.CreateSession.
ms.assetid: 22a8107a-8e5e-4636-bf7d-a261f885e074
ms.tgt_platform: multiple
keywords:
- Método SessionFlagUseNoAuthentication Windows administración remota
- Método SessionFlagUseNoAuthentication Windows administración remota , objeto WSMan
- WSMan object Windows Remote Management , SessionFlagUseNoAuthentication (método)
topic_type:
- apiref
api_name:
- WSMan.SessionFlagUseNoAuthentication
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1edb428a8c739c224e55bd4437dfdd6f544e9adf3039afb61df659b4969fb9ef
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119412405"
---
# <a name="wsmansessionflagusenoauthentication-method"></a>Método WSMan.SessionFlagUseNoAuthentication

El **método WSMan.SessionFlagUseNoAuthentication** devuelve el valor de la marca de autenticación **WSManFlagUseNoAuthentication** para su uso en el parámetro *flags* del método [**WSMan.CreateSession.**](wsman-createsession.md) Este método proporciona una sintaxis más eficaz para usar la constante para que los scripts no sean necesarios para establecer un valor constante. Para obtener más información sobre cómo llamar a este método, vea [Constantes de sesión](session-constants.md).

**WSManFlagUseNoAuthentication es** una constante en la **\_ \_ enumeración WSManSessionFlags.** Para obtener más información, vea // Authentication Constants ([Constantes de autenticación ).](authentication-constants.md)

## <a name="syntax"></a>Sintaxis


```VB
WSMan.SessionFlagUseNoAuthentication( _
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

 

 





