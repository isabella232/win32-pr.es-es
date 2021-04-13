---
title: Propiedad ResourceLocator. FragmentDialect (WSManDisp. h)
description: Obtiene o establece el dialecto de lenguaje para un dialecto de fragmento de recurso cuando se usa ResourceLocator en operaciones de objeto de sesión como Session. get, Session. put o Session. Enumerate.
ms.assetid: 60b08084-f4b9-4049-b0cd-a7420fcffd7c
ms.tgt_platform: multiple
keywords:
- Administración remota de Windows de la propiedad FragmentDialect
- Administración remota de Windows de la propiedad FragmentDialect, objeto ResourceLocator
- Administración remota de Windows de objeto ResourceLocator, propiedad FragmentDialect
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
ms.openlocfilehash: f1fe42c2bbe15c75d5f38ea47119f9649e678931
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492676"
---
# <a name="resourcelocatorfragmentdialect-property"></a>Propiedad ResourceLocator. FragmentDialect

Obtiene o establece el dialecto de lenguaje para un *dialecto* de [*fragmento*](windows-remote-management-glossary.md) de [*recurso*](windows-remote-management-glossary.md) cuando se usa [**ResourceLocator**](resourcelocator.md) en operaciones de objeto de [**sesión**](session.md) como [**Session. Get**](session-get.md), [**Session. put**](session-put.md)o [**Session. Enumerate**](session-enumerate.md). Un fragmento representa una propiedad o parte de un recurso. Puede proporcionar un objeto [**ResourceLocator**](resourcelocator.md) en lugar de especificar un URI de recurso en las operaciones del objeto de [**sesión**](session.md) . El dialecto indica qué lenguaje XML describe el fragmento para el servicio que implementa el [protocolo WS-Management](ws-management-protocol.md) y recibe la solicitud.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```VB
ResourceLocator.FragmentDialect As string
```



## <a name="property-value"></a>Valor de propiedad

Cadena XML que identifica el idioma usado en la propiedad [**FragmentPath**](resourcelocator-fragmentpath.md) . La cadena de dialecto tiene como valor predeterminado la especificación XPath 1,0. Para más información, consulte [https://www.w3.org/TR/xpath](https://www.w3.org/TR/xpath).

## <a name="remarks"></a>Observaciones

[**IWSManResourceLocator:: FragmentDialect**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanresourcelocator-get_fragmentdialect) es la propiedad de C++ correspondiente.

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

 

 





