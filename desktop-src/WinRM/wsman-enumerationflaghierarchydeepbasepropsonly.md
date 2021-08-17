---
title: Método WSMan.EnumerationFlagHierarchyDeepBasePropsOnly (WSManDisp.h)
description: Devuelve el valor de la marca de enumeración EnumerationFlagHierarchyDeepBasePropsOnly para su uso en el parámetro flags de Session.Enumerate.
ms.assetid: f4c5966a-0d9f-4d93-9ccd-2e8a5f32b77f
ms.tgt_platform: multiple
keywords:
- Método EnumerationFlagHierarchyDeepBasePropsOnly Windows administración remota
- Método EnumerationFlagHierarchyDeepBasePropsOnly Windows de administración remota , objeto WSMan
- Objeto WSMan Windows administración remota, método EnumerationFlagHierarchyDeepBasePropsOnly
topic_type:
- apiref
api_name:
- WSMan.EnumerationFlagHierarchyDeepBasePropsOnly
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 197c615b8d805fc142fa8afb2cf4fbb56ef22eec76caf63f03c27f3d9f131b82
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117742463"
---
# <a name="wsmanenumerationflaghierarchydeepbasepropsonly-method"></a>Método WSMan.EnumerationFlagHierarchyDeepBasePropsOnly

El **método WSMan.EnumerationFlagHierarchyDeepBasePropsOnly** devuelve el valor de la marca de enumeración **EnumerationFlagHierarchyDeepBasePropsOnly** para su uso en el parámetro *flags* [**de Session.Enumerate**](session-enumerate.md). Este método proporciona una sintaxis más eficaz para usar la constante para que los scripts no sean necesarios para establecer un valor constante. Para obtener más información sobre cómo llamar a este método, vea [Constantes de sesión](session-constants.md).

**EnumerationFlagHierarchyDeepBasePropsOnly** es una constante en la enumeración **\_ WSManEnumFlags** y se describe en [**Constantes de enumeración**](enumeration-constants.md).

## <a name="syntax"></a>Sintaxis


```VB
WSMan.EnumerationFlagHierarchyDeepBasePropsOnly( _
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

 

 





