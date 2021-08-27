---
title: Método ResourceLocator.AddSelector (WSManDisp.h)
description: Agrega un selector al objeto ResourceLocator. El selector especifica una instancia determinada de un recurso.
ms.assetid: 4b513d39-a377-487f-a03b-f3c5ab0f0b5a
ms.tgt_platform: multiple
keywords:
- Método AddSelector Windows Administración remota
- Método AddSelector Windows administración remota, objeto ResourceLocator
- Objeto ResourceLocator Windows administración remota, método AddSelector
topic_type:
- apiref
api_name:
- ResourceLocator.AddSelector
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6fc59aab6e5194716fa3b0cda98bb874d0045011c0159c5caaa3cbd53e7fbfd5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120121645"
---
# <a name="resourcelocatoraddselector-method"></a>Método ResourceLocator.AddSelector

Agrega un [*selector*](windows-remote-management-glossary.md) al [**objeto ResourceLocator.**](resourcelocator.md) El selector especifica una instancia determinada de un *recurso*. Puede proporcionar un objeto [**ResourceLocator**](resourcelocator.md) en lugar [](session.md) de especificar un URI de recurso en operaciones de objeto de sesión como [**Session.Get**](session-get.md), [**Session.Put**](session-put.md)o [**Session.Enumerate**](session-enumerate.md).

## <a name="syntax"></a>Sintaxis


```VB
ResourceLocator.AddSelector( _
  ByVal resourceSelName, _
  ByVal selValue _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*resourceSelName* \[ En\]
</dt> <dd>

Nombre del selector. Por ejemplo, al solicitar datos WMI, este parámetro es la propiedad clave de una clase WMI.

</dd> <dt>

*selValue* \[ En\]
</dt> <dd>

Valor del selector. Por ejemplo, para los datos WMI, este parámetro contiene un valor para una propiedad de clave que identifica una instancia específica.

</dd> </dl>

## <a name="remarks"></a>Comentarios

**IWSManResourceLocator::AddSelector es** el método de C++ correspondiente.

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

[**ResourceLocator**](resourcelocator.md)
</dt> </dl>

 

 





