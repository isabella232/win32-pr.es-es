---
title: Propiedad ResourceLocator. MustUnderstandOptions (WSManDisp. h)
description: Obtiene o establece el valor de MustUnderstandOptions para el objeto ResourceLocator.
ms.assetid: d366696c-9128-4cbd-98d0-6c2d16c75d59
ms.tgt_platform: multiple
keywords:
- Administración remota de Windows de la propiedad MustUnderstandOptions
- Administración remota de Windows de la propiedad MustUnderstandOptions, objeto ResourceLocator
- Administración remota de Windows de objeto ResourceLocator, propiedad MustUnderstandOptions
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
ms.openlocfilehash: 2945efd1a224c333f45956a29df779efc98e944f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996975"
---
# <a name="resourcelocatormustunderstandoptions-property"></a>Propiedad ResourceLocator. MustUnderstandOptions

Obtiene o establece el valor de **MustUnderstandOptions** para el objeto [**ResourceLocator**](resourcelocator.md) . Puede proporcionar un objeto [**ResourceLocator**](resourcelocator.md) en lugar de especificar un URI de recurso en operaciones de objetos de [**sesión**](session.md) como [**Session. Get**](session-get.md), [**Session. put**](session-put.md)o [**Session. Enumerate**](session-enumerate.md).

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```VB
ResourceLocator.MustUnderstandOptions As boolean
```



## <a name="property-value"></a>Valor de propiedad

Indica que, cuando es **true**, el servicio que implementa el [protocolo WS-Management](ws-management-protocol.md) debe devolver un error si no es capaz de procesar la opción.

## <a name="remarks"></a>Observaciones

**IWSManResourceLocator:: MustUnderstandOptions** es la propiedad de C++ correspondiente.

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

[**ResourceLocator**](resourcelocator.md)
</dt> </dl>

 

 





