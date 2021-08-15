---
title: Método WSMan.EnumerationFlagReturnEPR (WSManDisp.h)
description: Devuelve el valor de la marca de enumeración EnumerationFlagReturnEPR para su uso en el parámetro flags de Session.Enumerate.
ms.assetid: 5e168aa9-5be1-46b3-bb9b-59895e68a75d
ms.tgt_platform: multiple
keywords:
- Método EnumerationFlagReturnEPR Windows remote management
- Método EnumerationFlagReturnEPR Windows remote management , objeto WSMan
- WSMan object Windows Remote Management , EnumerationFlagReturnEPR method
topic_type:
- apiref
api_name:
- WSMan.EnumerationFlagReturnEPR
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f464dddc35a7976b5231b116a5e51322b86e2941d9a2cd5a476b86b600130ef1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117742274"
---
# <a name="wsmanenumerationflagreturnepr-method"></a>Método WSMan.EnumerationFlagReturnEPR

El **método EnumerationFlagReturnEPR** devuelve el valor de la marca de enumeración **EnumerationFlagReturnEPR** para su uso en el parámetro *flags* [**de Session.Enumerate**](session-enumerate.md). Este método proporciona una sintaxis más eficaz para usar la constante para que los scripts no sean necesarios para establecer un valor constante. Para obtener más información sobre cómo llamar a este método, vea [Constantes de sesión](session-constants.md).

**EnumerationFlagReturnEPR es** una constante de la enumeración **\_ WSManEnumFlags** y se describe en [**Constantes de enumeración**](enumeration-constants.md).

## <a name="syntax"></a>Sintaxis


```VB
WSMan.EnumerationFlagReturnEPR( _
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



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                 |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                           |
| Header<br/>                   | <dl> <dt>WSManDisp.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>WSManDisp.idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>WSManDisp.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**WSMan**](wsman.md)
</dt> <dt>

[**Sesión**](session.md)
</dt> </dl>

 

 





