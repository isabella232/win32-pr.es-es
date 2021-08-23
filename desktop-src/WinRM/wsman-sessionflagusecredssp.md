---
title: Método WSMan.SessionFlagUseCredSsp (WSManDisp.h)
description: Devuelve el valor de la marca de autenticación WSManFlagUseCredSsp para su uso en el parámetro flags del método WSMan.CreateSession.
ms.assetid: bb167445-91d6-4e06-a976-bf869320784a
ms.tgt_platform: multiple
keywords:
- Método SessionFlagUseCredSsp Windows administración remota
- Método SessionFlagUseCredSsp Windows de administración remota , objeto WSMan
- Objeto WSMan Windows administración remota , método SessionFlagUseCredSsp
topic_type:
- apiref
api_name:
- WSMan.SessionFlagUseCredSsp
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27eb96f1de72bbcceafd40c0ccbcfdd3b990ed2134739195bd29e130dbac5a64
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119642235"
---
# <a name="wsmansessionflagusecredssp-method"></a>Método WSMan.SessionFlagUseCredSsp

Devuelve el valor de la marca de autenticación **WSManFlagUseCredSsp** para su uso en el parámetro *flags* del [**método WSMan.CreateSession.**](wsman-createsession.md) Este método proporciona una sintaxis más eficaz para usar la constante para que los scripts no sean necesarios para establecer un valor constante. Para obtener más información sobre cómo llamar a este método, vea [Constantes de sesión](session-constants.md).

**WSManFlagUseCredSsp es** una constante en la **\_ \_ enumeración WSManSessionFlags.** Para obtener más información, vea [Constantes de autenticación](authentication-constants.md).

## <a name="syntax"></a>Sintaxis


```VB
WSMan.SessionFlagUseCredSsp( _
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
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7<br/>                                                                                                        |
| Servidor mínimo compatible<br/> | Windows Server 2008 R2<br/>                                                                                           |
| Redistribuible<br/>          | Windows Management Framework en Windows Server 2008 con SP2, Windows Vista con SP1 y Windows Vista con SP2<br/> |
| Header<br/>                   | <dl> <dt>WSManDisp.h</dt> </dl>                                      |
| Idl<br/>                      | <dl> <dt>WSManDisp.idl</dt> </dl>                                    |
| Biblioteca<br/>                  | <dl> <dt>WSManDisp.tlb</dt> </dl>                                    |
| Archivo DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>                                      |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**WSMan**](wsman.md)
</dt> <dt>

[**Sesión**](session.md)
</dt> </dl>

 

 





