---
title: Método WSMan.SessionFlagEnableSPNServerPort (WSManDisp.h)
description: Devuelve el valor de la marca de autenticación WSManFlagEnableSPNServerPort para su uso en el parámetro flags del método WSMan.CreateSession.
ms.assetid: a18a87e6-dcee-4e9f-8e8c-262fef36ab1a
ms.tgt_platform: multiple
keywords:
- Método SessionFlagEnableSPNServerPort Windows administración remota
- Método SessionFlagEnableSPNServerPort Windows de administración remota , objeto WSMan
- Objeto WSMan Windows administración remota , método SessionFlagEnableSPNServerPort
topic_type:
- apiref
api_name:
- WSMan.SessionFlagEnableSPNServerPort
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5eb309f8fd9d6351ff34201ec409256bad5160ef2cd0224f5cdbf5263ae05214
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119758935"
---
# <a name="wsmansessionflagenablespnserverport-method"></a>Método WSMan.SessionFlagEnableSPNServerPort

El **método WSMan.SessionFlagEnableSPNServerPort** devuelve el valor de la marca de autenticación **WSManFlagEnableSPNServerPort** para su uso en el parámetro *flags* del método [**WSMan.CreateSession.**](wsman-createsession.md) Este método proporciona una sintaxis más eficaz para usar la constante para que los scripts no sean necesarios para establecer un valor constante. Para obtener más información sobre cómo llamar a este método, vea [Constantes de sesión](session-constants.md).

**WSManFlagEnableSPNServerPort** es una constante en la **\_ \_ enumeración WSManSessionFlags.** Para obtener más información, vea [**Otras constantes de sesión**](other-session-constants.md).

## <a name="syntax"></a>Sintaxis


```VB
WSMan.SessionFlagEnableSPNServerPort( _
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

 

 





