---
title: Método WSMan.SessionFlagSkipCACheck (WSManDisp.h)
description: Devuelve el valor de la marca de autenticación WSManFlagSkipCACheck para su uso en el parámetro flags de WSMan.CreateSession.
ms.assetid: a67cadb3-c20a-4a58-a13b-5bbd23c547d1
ms.tgt_platform: multiple
keywords:
- Método SessionFlagSkipCACheck Windows administración remota
- Método SessionFlagSkipCACheck Windows de administración remota , objeto WSMan
- Objeto WSMan Windows administración remota, método SessionFlagSkipCACheck
topic_type:
- apiref
api_name:
- WSMan.SessionFlagSkipCACheck
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe24e10ca7a568a6dc9b3af6efed6e31a3a9fde5acac70e2badab37d24373350
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117742034"
---
# <a name="wsmansessionflagskipcacheck-method"></a>Método WSMan.SessionFlagSkipCACheck

El **método WSMan.SessionFlagSkipCACheck** devuelve el valor de la marca de autenticación **WSManFlagSkipCACheck** para su uso en el parámetro *flags* de [**WSMan.CreateSession**](wsman-createsession.md). Este método proporciona una sintaxis más eficaz para usar la constante para que los scripts no sean necesarios para establecer un valor constante. Para obtener más información sobre cómo llamar a este método y ejemplos de código, vea [Constantes de sesión](session-constants.md).

**WSManFlagSkipCACheck es** una constante en la **\_ \_ enumeración WSManSessionFlags.** Para obtener más información, vea [**Constantes de autenticación**](authentication-constants.md).

## <a name="syntax"></a>Sintaxis


```VB
WSMan.SessionFlagSkipCACheck( _
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

 

 





