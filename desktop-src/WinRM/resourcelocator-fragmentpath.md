---
title: Propiedad ResourceLocator. FragmentPath (WSManDisp. h)
description: Obtiene o establece la ruta de acceso de un fragmento de recursos o propiedad cuando se usa ResourceLocator en operaciones de objeto de sesión como Session. get, Session. put o Session. Enumerate.
ms.assetid: 4d059b57-fca5-4a75-9396-6505920498c3
ms.tgt_platform: multiple
keywords:
- Administración remota de Windows de la propiedad FragmentPath
- Administración remota de Windows de la propiedad FragmentPath, objeto ResourceLocator
- Administración remota de Windows de objeto ResourceLocator, propiedad FragmentPath
topic_type:
- apiref
api_name:
- ResourceLocator.FragmentPath
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e15fba102f9a7c8a2581271c575857b49bc5df1c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079411"
---
# <a name="resourcelocatorfragmentpath-property"></a>Propiedad ResourceLocator. FragmentPath

Obtiene o establece la ruta de acceso de un [*fragmento*](windows-remote-management-glossary.md) de [*recursos*](windows-remote-management-glossary.md) o propiedad cuando se usa [**ResourceLocator**](resourcelocator.md) en operaciones de objeto de [**sesión**](session.md) como [**Session. Get**](session-get.md), [**Session. put**](session-put.md)o [**Session. Enumerate**](session-enumerate.md).

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```VB
ResourceLocator.FragmentPath
```



## <a name="property-value"></a>Valor de propiedad

Cadena que identifica el fragmento o la propiedad del recurso. Por ejemplo, si el recurso es una unidad de disco y la propiedad solicitada es fabricante, la cadena puede contener `Diskdrive/Manufacturer` . El texto del fragmento distingue mayúsculas de minúsculas. En este caso, no se puede usar `diskdrive/manufacturer` .

## <a name="remarks"></a>Observaciones

**IWSManResourceLocator:: FragmentPath** es la propiedad de C++ correspondiente.

Puede especificar un elemento de una propiedad de matriz proporcionando el índice de la matriz como se muestra en el ejemplo siguiente. Tenga en cuenta que la indización de matriz empieza por 1 en lugar de 0.


```VB
Const Uri = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_NetworkAdapterConfiguration"
Const FragmentPath = "DNSServerSearchOrder[1]"
```



Para obtener toda la matriz, especifique el nombre de la propiedad de matriz como se muestra en el ejemplo siguiente.


```VB
Const Uri = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_NetworkAdapterConfiguration"
Const FragmentPath = "DNSServerSearchOrder"
```



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

 

 





