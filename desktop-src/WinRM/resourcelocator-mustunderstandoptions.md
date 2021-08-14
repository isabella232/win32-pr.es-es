---
title: Propiedad ResourceLocator.MustUnderstandOptions (WSManDisp.h)
description: Obtiene o establece el valor MustUnderstandOptions para el objeto ResourceLocator.
ms.assetid: d366696c-9128-4cbd-98d0-6c2d16c75d59
ms.tgt_platform: multiple
keywords:
- Propiedad MustUnderstandOptions Windows administración remota
- Propiedad MustUnderstandOptions Windows administración remota , objeto ResourceLocator
- Objeto ResourceLocator Windows administración remota , propiedad MustUnderstandOptions
topic_type:
- apiref
api_name:
- ResourceLocator.MustUnderstandOptions
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a49c3af0372553c221dae902a5fdca0e026bb874f612b8e21f41e6a6870f7ea8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118323743"
---
# <a name="resourcelocatormustunderstandoptions-property"></a>Propiedad ResourceLocator.MustUnderstandOptions

Obtiene o establece el **valor MustUnderstandOptions** para el [**objeto ResourceLocator.**](resourcelocator.md) Puede proporcionar un objeto [**ResourceLocator**](resourcelocator.md) en lugar de especificar un URI de recurso en operaciones de objeto [**de**](session.md) sesión como [**Session.Get**](session-get.md), [**Session.Put**](session-put.md)o [**Session.Enumerate.**](session-enumerate.md)

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Syntax


```VB
ResourceLocator.MustUnderstandOptions As boolean
```



## <a name="property-value"></a>Valor de propiedad

Indica, cuando **es True**, que [](ws-management-protocol.md) el servicio que implementa el protocolo WS-Management debe devolver un error si no es capaz de procesar la opción.

## <a name="remarks"></a>Comentarios

**IWSManResourceLocator::MustUnderstandOptions** es la propiedad de C++ correspondiente.

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

[**ResourceLocator**](resourcelocator.md)
</dt> </dl>

 

 





