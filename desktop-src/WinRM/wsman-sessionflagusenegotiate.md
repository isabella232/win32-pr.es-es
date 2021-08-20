---
title: Método WSMan.SessionFlagUseNegotiate (WSManDisp.h)
description: Devuelve el valor de la marca de autenticación WSManFlagUseNegotiate para su uso en el parámetro flags del método WSMan.CreateSession.
ms.assetid: 86d8ed13-5eae-4a06-8ceb-b0ec067f4a4c
ms.tgt_platform: multiple
keywords:
- Método SessionFlagUseNegotiate Windows remote management
- Método SessionFlagUseNegotiate Windows administración remota , objeto WSMan
- Objeto WSMan Windows administración remota , método SessionFlagUseNegotiate
topic_type:
- apiref
api_name:
- WSMan.SessionFlagUseNegotiate
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d7a6af51cad3a1e0ea5c78aee92e9650af16d6b0d699d28a7d9d48cb51d0784
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118823277"
---
# <a name="wsmansessionflagusenegotiate-method"></a>Método WSMan.SessionFlagUseNegotiate

El **método WSMan.SessionFlagUseNegotiate** devuelve el valor de la marca de autenticación **WSManFlagUseNegotiate** para su uso en el parámetro *flags* del método [**WSMan.CreateSession.**](wsman-createsession.md) Este método proporciona una sintaxis más eficaz para usar la constante para que los scripts no sean necesarios para establecer un valor constante. Para obtener más información sobre cómo llamar a este método, vea [Constantes de sesión](session-constants.md).

**WSManFlagUseNegotiate es** una constante en la **\_ \_ enumeración WSManSessionFlags.** Para obtener más información, vea [Constantes de autenticación](authentication-constants.md).

## <a name="syntax"></a>Sintaxis


```VB
WSMan.SessionFlagUseNegotiate( _
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

 

 





