---
title: Método WSMan. SessionFlagUseNoAuthentication (WSManDisp. h)
description: Devuelve el valor de la marca de autenticación WSManFlagUseNoAuthentication para su uso en el parámetro flags del método WSMan. CreateSession.
ms.assetid: 22a8107a-8e5e-4636-bf7d-a261f885e074
ms.tgt_platform: multiple
keywords:
- Método SessionFlagUseNoAuthentication Administración remota de Windows
- Administración remota de Windows método SessionFlagUseNoAuthentication, objeto WSMan
- Administración remota de Windows de objeto WSMan, método SessionFlagUseNoAuthentication
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
ms.openlocfilehash: 6b9676d3baa9a18ae8a3feb5eb4092c63586a94b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492670"
---
# <a name="wsmansessionflagusenoauthentication-method"></a>WSMan. SessionFlagUseNoAuthentication (método)

El método **wsman. SessionFlagUseNoAuthentication** devuelve el valor de la marca de autenticación **WSManFlagUseNoAuthentication** para su uso en el parámetro *Flags* del método [**WSMan. createSession**](wsman-createsession.md) . Este método proporciona una sintaxis más eficaz para usar la constante, de modo que los scripts no sean necesarios para establecer un valor constante. Para obtener más información sobre cómo llamar a este método, vea [constantes de sesión](session-constants.md).

**WSManFlagUseNoAuthentication** es una constante de la enumeración **\_ \_ WSManSessionFlags** . Para obtener más información, vea//[constantes de autenticación](authentication-constants.md).

## <a name="syntax"></a>Sintaxis


```VB
WSMan.SessionFlagUseNoAuthentication( _
  ByRef flags _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*marcas* \[ de enuncia\]
</dt> <dd>

Valor de la constante.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                 |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                           |
| Encabezado<br/>                   | <dl> <dt>WSManDisp. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WSManDisp. idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>WSManDisp. tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**WSMan**](wsman.md)
</dt> <dt>

[**De sesión**](session.md)
</dt> </dl>

 

 





