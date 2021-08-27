---
title: Propiedad ResourceLocator.FragmentPath (WSManDisp.h)
description: Obtiene o establece la ruta de acceso de un fragmento de recursos o una propiedad cuando se usa ResourceLocator en operaciones de objeto de sesión como Session.Get, Session.Put o Session.Enumerate.
ms.assetid: 4d059b57-fca5-4a75-9396-6505920498c3
ms.tgt_platform: multiple
keywords:
- Propiedad FragmentPath Windows administración remota
- Propiedad FragmentPath Windows administración remota, objeto ResourceLocator
- Objeto ResourceLocator Windows administración remota, propiedad FragmentPath
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
ms.openlocfilehash: 26f756d669ba79ce034a9562d6cae5d58653bc60e042344306fb18aa37edfdc6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120121635"
---
# <a name="resourcelocatorfragmentpath-property"></a>Propiedad ResourceLocator.FragmentPath

Obtiene o establece la ruta de acceso de un [](session.md) fragmento de recursos o una propiedad cuando se usa [**ResourceLocator**](resourcelocator.md) en operaciones de objeto de sesión como [**Session.Get**](session-get.md), [**Session.Put**](session-put.md)o [**Session.Enumerate.**](session-enumerate.md) [](windows-remote-management-glossary.md) [](windows-remote-management-glossary.md)

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Syntax


```VB
ResourceLocator.FragmentPath
```



## <a name="property-value"></a>Valor de propiedad

Cadena que identifica el fragmento o la propiedad del recurso. Por ejemplo, si el recurso es una unidad de disco y la propiedad solicitada es Fabricante, la cadena puede contener `Diskdrive/Manufacturer` . El texto del fragmento distingue mayúsculas de minúsculas. En este caso, no puede usar `diskdrive/manufacturer` .

## <a name="remarks"></a>Comentarios

**IWSManResourceLocator::FragmentPath** es la propiedad de C++ correspondiente.

Puede especificar un elemento de una propiedad de matriz si proporciona el índice de la matriz como se muestra en el ejemplo siguiente. Tenga en cuenta que la indexación de matrices comienza con 1 en lugar de con 0.


```VB
Const Uri = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_NetworkAdapterConfiguration"
Const FragmentPath = "DNSServerSearchOrder[1]"
```



Para obtener toda la matriz, especifique el nombre de la propiedad de la matriz como se muestra en el ejemplo siguiente.


```VB
Const Uri = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_NetworkAdapterConfiguration"
Const FragmentPath = "DNSServerSearchOrder"
```



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

 

 





