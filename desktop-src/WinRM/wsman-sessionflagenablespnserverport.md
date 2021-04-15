---
title: Método WSMan. SessionFlagEnableSPNServerPort (WSManDisp. h)
description: Devuelve el valor de la marca de autenticación WSManFlagEnableSPNServerPort para su uso en el parámetro flags del método WSMan. CreateSession.
ms.assetid: a18a87e6-dcee-4e9f-8e8c-262fef36ab1a
ms.tgt_platform: multiple
keywords:
- Método SessionFlagEnableSPNServerPort Administración remota de Windows
- Administración remota de Windows método SessionFlagEnableSPNServerPort, objeto WSMan
- Administración remota de Windows de objeto WSMan, método SessionFlagEnableSPNServerPort
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
ms.openlocfilehash: 4153f088079b58b3b0e048f2cd8f38b3524754a0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534522"
---
# <a name="wsmansessionflagenablespnserverport-method"></a>WSMan. SessionFlagEnableSPNServerPort (método)

El método **wsman. SessionFlagEnableSPNServerPort** devuelve el valor de la marca de autenticación **WSManFlagEnableSPNServerPort** para su uso en el parámetro *Flags* del método [**WSMan. createSession**](wsman-createsession.md) . Este método proporciona una sintaxis más eficaz para usar la constante, de modo que los scripts no sean necesarios para establecer un valor constante. Para obtener más información sobre cómo llamar a este método, vea [constantes de sesión](session-constants.md).

**WSManFlagEnableSPNServerPort** es una constante de la enumeración **\_ \_ WSManSessionFlags** . Para obtener más información, vea [**otras constantes de sesión**](other-session-constants.md).

## <a name="syntax"></a>Sintaxis


```VB
WSMan.SessionFlagEnableSPNServerPort( _
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

 

 





