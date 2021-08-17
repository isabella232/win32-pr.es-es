---
title: Método WSMan.EnumerationFlagNonXmlText (WSManDisp.h)
description: Devuelve el valor de la constante de enumeración WSManFlagNonXmlText para su uso en el parámetro flags del método Session.Enumerate.
ms.assetid: 5e062e73-f833-4090-ba5a-48ca374724e7
ms.tgt_platform: multiple
keywords:
- Método EnumerationFlagNonXmlText Windows Remote Management
- Método EnumerationFlagNonXmlText Windows administración remota , objeto WSMan
- WSMan object Windows Remote Management , EnumerationFlagNonXmlText method
topic_type:
- apiref
api_name:
- WSMan.EnumerationFlagNonXmlText
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6606a20d0ab7f59b7521367243ccdc97fd90209f1791d8f1ded3e48c70e3f59
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117742294"
---
# <a name="wsmanenumerationflagnonxmltext-method"></a>Método WSMan.EnumerationFlagNonXmlText

**WSMan.EnumerationFlagNonXmlText** devuelve el valor de la constante de enumeración **WSManFlagNonXmlText** para su uso en el parámetro *flags* del [**método Session.Enumerate.**](session-enumerate.md) Este método proporciona una sintaxis más eficaz para usar la constante para que los scripts no sean necesarios para establecer un valor constante. Para obtener más información sobre cómo llamar a este método, vea [Constantes de sesión](session-constants.md).

**WSManFlagNonXmlText es** una constante en la **\_ \_ enumeración WSManEnumFlags.** Para obtener más información, vea [**Constantes de enumeración**](enumeration-constants.md).

## <a name="syntax"></a>Sintaxis


```VB
WSMan.EnumerationFlagNonXmlText( _
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

[**IWSManEx**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanex)
</dt> <dt>

[**IWSManSession**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmansession)
</dt> </dl>

 

 





