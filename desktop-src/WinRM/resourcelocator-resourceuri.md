---
title: Propiedad ResourceLocator. ResourceURI (WSManDisp. h)
description: Obtiene o establece el URI de recurso en un objeto ResourceLocator.
ms.assetid: adb1e08a-290f-4a23-a6e4-d7567a6b7eee
ms.tgt_platform: multiple
keywords:
- Propiedad ResourceURI Administración remota de Windows
- Propiedad ResourceURI Administración remota de Windows, objeto ResourceLocator
- Administración remota de Windows objeto ResourceLocator, ResourceURI (propiedad)
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
ms.openlocfilehash: 28f804835b5445c32f74094e8280a598785d1526
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491579"
---
# <a name="resourcelocatorresourceuri-property"></a>Propiedad ResourceLocator. ResourceURI

Obtiene o establece el [*URI de recurso*](windows-remote-management-glossary.md) en un objeto [**ResourceLocator**](resourcelocator.md) . Puede proporcionar un objeto [**ResourceLocator**](resourcelocator.md) en lugar de especificar un URI de recurso en operaciones de objetos de [**sesión**](session.md) como [**Session. Get**](session-get.md), [**Session. put**](session-put.md)o [**Session. Enumerate**](session-enumerate.md).

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```VB
ResourceLocator.ResourceURI As string
```



## <a name="property-value"></a>Valor de propiedad

Cadena que identifica el recurso. Al establecer el URI de recurso para un objeto [**ResourceLocator**](resourcelocator.md) , el URI debe contener solo la ruta de acceso.

## <a name="remarks"></a>Observaciones

El siguiente es un ejemplo de una ruta de acceso adecuada para [**ResourceURI**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanresourcelocator-get_resourceuri).

``` syntax
"http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Service"
```

La ruta de acceso siguiente no funciona porque contiene una clave para una instancia específica. Use el método [**ResourceLocator. AddSelector**](resourcelocator-addselector.md) para especificar una instancia determinada.

``` syntax
"http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Service?Name=winmgmt"
```

**IWSManResourceLocator:: ResourceURI** es el método de C++ correspondiente.

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

 

 





