---
title: Método WSMan.SessionFlagUseKerberos (WSManDisp.h)
description: Devuelve el valor de la marca de autenticación WSManFlagUseKerberos para su uso en el parámetro flags de WSMan.CreateSession.
ms.assetid: be005312-1e87-4371-9791-709a9be46f7c
ms.tgt_platform: multiple
keywords:
- Método SessionFlagUseKerberos Windows administración remota
- Método SessionFlagUseKerberos Windows remote management , objeto WSMan
- Objeto WSMan Windows administración remota , método SessionFlagUseKerberos
topic_type:
- apiref
api_name:
- WSMan.SessionFlagUseKerberos
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 468d6096343e3c0fe67369abe3927870f2e1eaf89a2d12b9c73e3560d436859e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119997214"
---
# <a name="wsmansessionflagusekerberos-method"></a>Método WSMan.SessionFlagUseKerberos

El **método WSMan.SessionFlagUseKerberos** devuelve el valor de la marca de autenticación **WSManFlagUseKerberos** para su uso en el parámetro *flags* de [**WSMan.CreateSession**](wsman-createsession.md). Este método proporciona una sintaxis más eficaz para usar la constante para que los scripts no sean necesarios para establecer un valor constante. Para obtener más información sobre cómo llamar a este método, vea [Constantes de sesión](session-constants.md).

**WSManFlagUseKerberos es una** constante en la **\_ \_ enumeración WSManSessionFlags.** Para obtener más información, vea [Constantes de autenticación](authentication-constants.md).

## <a name="syntax"></a>Sintaxis


```VB
WSMan.SessionFlagUseKerberos( _
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

 

 





