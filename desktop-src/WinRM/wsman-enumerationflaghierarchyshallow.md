---
title: Método WSMan.EnumerationFlagHierarchyShallow (WSManDisp.h)
description: Devuelve el valor de la marca de enumeración EnumerationFlagHierarchyShallow para su uso en el parámetro flags de Session.Enumerate.
ms.assetid: 18b564e6-dda1-44b9-b445-26c6183b6af9
ms.tgt_platform: multiple
keywords:
- Método EnumerationFlagHierarchyShallow Windows Remote Management
- Método EnumerationFlagHierarchyShallow Windows remote management , objeto WSMan
- Objeto WSMan Windows administración remota , método EnumerationFlagHierarchyShallow
topic_type:
- apiref
api_name:
- WSMan.EnumerationFlagHierarchyShallow
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f894c252de856a6845b1d98b475a51e92dc1d95b054eb77449617f6fc36bf87
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117742304"
---
# <a name="wsmanenumerationflaghierarchyshallow-method"></a>Método WSMan.EnumerationFlagHierarchyShallow

El **método EnumerationFlagHierarchyShallow** devuelve el valor de la marca de enumeración **EnumerationFlagHierarchyShallow** para su uso en el parámetro *flags* [**de Session.Enumerate**](session-enumerate.md). Este método proporciona una sintaxis más eficaz para usar la constante para que los scripts no sean necesarios para establecer un valor constante. Para obtener más información sobre cómo llamar a este método, vea [Constantes de sesión](session-constants.md).

**EnumerationFlagHierarchyShallow es una** constante de la enumeración **\_ WSManEnumFlags** y se describe en [**Constantes de enumeración**](enumeration-constants.md).

## <a name="syntax"></a>Sintaxis


```VB
WSMan.EnumerationFlagHierarchyShallow( _
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

 

 





