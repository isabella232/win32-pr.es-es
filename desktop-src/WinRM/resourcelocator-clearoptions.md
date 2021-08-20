---
title: Método ResourceLocator.ClearOptions (WSManDisp.h)
description: Quita todas las opciones del objeto ResourceLocator.
ms.assetid: 1b4d7f15-c56f-4b0d-9614-8376012abca7
ms.tgt_platform: multiple
keywords:
- Método ClearOptions Windows administración remota
- Método ClearOptions Windows administración remota , objeto ResourceLocator
- Objeto ResourceLocator Windows administración remota , método ClearOptions
topic_type:
- apiref
api_name:
- ResourceLocator.ClearOptions
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef695b949c62c0d56de45914e1a54996d4d7599f029d136ad78b03ac687365aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118112916"
---
# <a name="resourcelocatorclearoptions-method"></a>Método ResourceLocator.ClearOptions

Quita todas las [*opciones*](windows-remote-management-glossary.md) del [**objeto ResourceLocator.**](resourcelocator.md) Puede proporcionar un objeto [**ResourceLocator**](resourcelocator.md) en lugar de especificar un URI de recurso en operaciones de objeto [**de**](session.md) sesión como [**Session.Get**](session-get.md), [**Session.Put**](session-put.md)o [**Session.Enumerate.**](session-enumerate.md)

## <a name="syntax"></a>Sintaxis


```VB
ResourceLocator.ClearOptions()
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="remarks"></a>Comentarios

**IWSManResourceLocator::ClearOptions** es el método de C++ correspondiente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
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

 

 





