---
title: Método ResourceLocator. AddSelector (WSManDisp. h)
description: Agrega un selector al objeto ResourceLocator. El selector especifica una instancia concreta de un recurso.
ms.assetid: 4b513d39-a377-487f-a03b-f3c5ab0f0b5a
ms.tgt_platform: multiple
keywords:
- Método AddSelector Administración remota de Windows
- Método AddSelector Administración remota de Windows, objeto ResourceLocator
- Administración remota de Windows de objeto ResourceLocator, método AddSelector
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
ms.openlocfilehash: 064108f535c9f46dc074d1b37754e626dc3f1d40
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996440"
---
# <a name="resourcelocatoraddselector-method"></a>ResourceLocator. AddSelector, método

Agrega un [*selector*](windows-remote-management-glossary.md) al objeto [**ResourceLocator**](resourcelocator.md) . El selector especifica una instancia concreta de un *recurso*. Puede proporcionar un objeto [**ResourceLocator**](resourcelocator.md) en lugar de especificar un URI de recurso en operaciones de objetos de [**sesión**](session.md) como [**Session. Get**](session-get.md), [**Session. put**](session-put.md)o [**Session. Enumerate**](session-enumerate.md).

## <a name="syntax"></a>Sintaxis


```VB
ResourceLocator.AddSelector( _
  ByVal resourceSelName, _
  ByVal selValue _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*resourceSelName* \[ de\]
</dt> <dd>

Nombre del selector. Por ejemplo, al solicitar datos WMI, este parámetro es la propiedad clave de una clase WMI.

</dd> <dt>

*selValue* \[ de\]
</dt> <dd>

Valor del selector. Por ejemplo, para los datos de WMI, este parámetro contiene un valor para una propiedad de clave que identifica una instancia específica.

</dd> </dl>

## <a name="remarks"></a>Observaciones

**IWSManResourceLocator:: AddSelector** es el método de C++ correspondiente.

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

 

 





