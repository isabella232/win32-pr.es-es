---
title: Método WSMan. EnumerationFlagReturnObject (WSManDisp. h)
description: Devuelve el valor de la marca de enumeración EnumerationFlagReturnObject para su uso en el parámetro flags de Session. Enumerate.
ms.assetid: a1d82530-63d7-4050-9e82-e31bec93bf38
ms.tgt_platform: multiple
keywords:
- Método EnumerationFlagReturnObject Administración remota de Windows
- Administración remota de Windows método EnumerationFlagReturnObject, objeto WSMan
- Administración remota de Windows de objeto WSMan, método EnumerationFlagReturnObject
topic_type:
- apiref
api_name:
- WSMan.EnumerationFlagReturnObject
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3019f880503f91d1488a2b7a41574cadc2df987
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105714613"
---
# <a name="wsmanenumerationflagreturnobject-method"></a>WSMan. EnumerationFlagReturnObject (método)

El método **WSMan. EnumerationFlagReturnObject** devuelve el valor de la marca de enumeración **EnumerationFlagReturnObject** para su uso en el parámetro *Flags* de [**Session. Enumerate**](session-enumerate.md). Este método proporciona una sintaxis más eficaz para usar la constante, de modo que los scripts no sean necesarios para establecer un valor constante. Para obtener más información sobre cómo llamar a este método, vea [constantes de sesión](session-constants.md).

**EnumerationFlagReturnObject** es una constante de la enumeración **\_ WSManEnumFlags** y se describe en [**constantes de enumeración**](enumeration-constants.md).

## <a name="syntax"></a>Sintaxis


```VB
WSMan.EnumerationFlagReturnObject( _
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

 

 





