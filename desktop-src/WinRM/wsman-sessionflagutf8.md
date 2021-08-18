---
title: Método WSMan.SessionFlagUTF8 (WSManDisp.h)
description: Devuelve el valor de la marca de autenticación WSManFlagUTF8 para su uso en el parámetro flags de WSMan.CreateSession.
ms.assetid: a79e292a-364b-4bf3-ae66-6a15ad51524f
ms.tgt_platform: multiple
keywords:
- Método SessionFlagUTF8 Windows administración remota
- Método SessionFlagUTF8 Windows administración remota , objeto WSMan
- Objeto WSMan Windows administración remota, método SessionFlagUTF8
topic_type:
- apiref
api_name:
- WSMan.SessionFlagUTF8
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 44fe6cc1b5f18fa316656d2b6974bd47c8209277ed24ef2798479227f9876e30
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117741923"
---
# <a name="wsmansessionflagutf8-method"></a>Método WSMan.SessionFlagUTF8

El **método WSMan.SessionFlagUTF8** devuelve el valor de la marca de autenticación **WSManFlagUTF8** para su uso en el parámetro *flags* de [**WSMan.CreateSession**](wsman-createsession.md). Este método proporciona una sintaxis más eficaz para usar la constante para que los scripts no sean necesarios para establecer un valor constante. Para obtener más información sobre cómo llamar a este método, vea [Constantes de sesión](session-constants.md).

**WSManFlagUTF8 es** una constante en la **\_ \_ enumeración WSManSessionFlags.** Para obtener más información, [vea Otras constantes de sesión](other-session-constants.md).

## <a name="syntax"></a>Sintaxis


```VB
WSMan.SessionFlagUTF8( _
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

 

 





