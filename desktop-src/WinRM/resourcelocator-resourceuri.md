---
title: Propiedad ResourceLocator.ResourceURI (WSManDisp.h)
description: Obtiene o establece el URI del recurso en un objeto ResourceLocator.
ms.assetid: adb1e08a-290f-4a23-a6e4-d7567a6b7eee
ms.tgt_platform: multiple
keywords:
- Propiedad ResourceURI Windows administración remota
- Propiedad ResourceURI Windows administración remota, objeto ResourceLocator
- Objeto ResourceLocator Windows administración remota, propiedad ResourceURI
topic_type:
- apiref
api_name:
- ResourceLocator.ResourceURI
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 323240462dad32ba757897798b663b78b373ebb3ab3e60c3387dd7da8eef4c85
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119642865"
---
# <a name="resourcelocatorresourceuri-property"></a>Propiedad ResourceLocator.ResourceURI

Obtiene o establece el [*URI del recurso*](windows-remote-management-glossary.md) en un objeto [**ResourceLocator.**](resourcelocator.md) Puede proporcionar un objeto [**ResourceLocator**](resourcelocator.md) en lugar [](session.md) de especificar un URI de recurso en operaciones de objeto de sesión como [**Session.Get**](session-get.md), [**Session.Put**](session-put.md)o [**Session.Enumerate.**](session-enumerate.md)

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Syntax


```VB
ResourceLocator.ResourceURI As string
```



## <a name="property-value"></a>Valor de propiedad

Cadena que identifica el recurso. Al establecer el URI de recurso para [**un objeto ResourceLocator,**](resourcelocator.md) el URI solo debe contener la ruta de acceso.

## <a name="remarks"></a>Comentarios

A continuación se muestra un ejemplo de una ruta de acceso adecuada [**para ResourceURI.**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanresourcelocator-get_resourceuri)

``` syntax
"http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Service"
```

La ruta de acceso siguiente no funciona porque contiene una clave para una instancia específica. Use el [**método ResourceLocator.AddSelector**](resourcelocator-addselector.md) para especificar una instancia determinada.

``` syntax
"http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Service?Name=winmgmt"
```

**IWSManResourceLocator::ResourceURI** es el método de C++ correspondiente.

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

 

 





