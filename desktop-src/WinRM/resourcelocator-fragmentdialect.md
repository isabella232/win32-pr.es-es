---
title: Propiedad ResourceLocator.FragmentDialect (WSManDisp.h)
description: Obtiene o establece el dialecto de idioma de un dialecto de fragmento de recursos cuando se usa ResourceLocator en operaciones de objeto session como Session.Get, Session.Put o Session.Enumerate.
ms.assetid: 60b08084-f4b9-4049-b0cd-a7420fcffd7c
ms.tgt_platform: multiple
keywords:
- Propiedad FragmentDialect Windows administración remota
- Propiedad FragmentDialect Windows administración remota, objeto ResourceLocator
- Objeto ResourceLocator Windows administración remota, propiedad FragmentDialect
topic_type:
- apiref
api_name:
- ResourceLocator.FragmentDialect
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2ae7cbbd71b4ccad24ecaa17d0fd635761f661bcd6dc95ebc0345e9164adcd9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119997305"
---
# <a name="resourcelocatorfragmentdialect-property"></a>Propiedad ResourceLocator.FragmentDialect

Obtiene o establece el [](windows-remote-management-glossary.md) dialecto de idioma de un *dialecto* de [*fragmento*](windows-remote-management-glossary.md) de recursos cuando se usa [**ResourceLocator**](resourcelocator.md) en operaciones de objeto [**session**](session.md) como [**Session.Get**](session-get.md), [**Session.Put**](session-put.md)o [**Session.Enumerate.**](session-enumerate.md) Un fragmento representa una propiedad o parte de un recurso. Puede proporcionar un objeto [**ResourceLocator**](resourcelocator.md) en lugar de especificar un URI de recurso en operaciones [**de objeto de**](session.md) sesión. El dialecto indica qué lenguaje XML describe el fragmento al servicio que implementa el protocolo WS-Management [recibe](ws-management-protocol.md) la solicitud.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Syntax


```VB
ResourceLocator.FragmentDialect As string
```



## <a name="property-value"></a>Valor de propiedad

Cadena XML que identifica el lenguaje usado en la [**propiedad FragmentPath.**](resourcelocator-fragmentpath.md) La cadena de dialecto tiene como valor predeterminado la especificación XPath 1.0. Para más información, consulte [https://www.w3.org/TR/xpath](https://www.w3.org/TR/xpath).

## <a name="remarks"></a>Comentarios

[**IWSManResourceLocator::FragmentDialect es**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanresourcelocator-get_fragmentdialect) la propiedad de C++ correspondiente.

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

 

 





