---
description: Proporciona métodos estándar com para administrar elementos de datos de almacenamiento protegidos.
ms.assetid: 6a4200ed-c3cf-4d6c-8936-22261e670087
title: Interfaz IPStore (Pstore.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: d6404d182a0c46de222b64892caa8b0e853610c980bfb79d286f781277493cba
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119749715"
---
# <a name="ipstore-interface"></a>Interfaz IPStore

\[La Storage protegida (Pstore) está disponible para su uso en Windows Server 2003 y Windows XP. Solo está disponible para operaciones de solo lectura en Windows Server 2008 y Windows Vista, pero puede que no esté disponible en versiones posteriores. Pstore usa una implementación anterior de la protección de datos. Se recomienda encarecidamente a los desarrolladores que aprovechen la protección de datos más segura que proporcionan las funciones [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) y [**CryptUnprotectData.**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata)\]

\[Esta interfaz puede modificarse o no estar disponible en versiones futuras de Windows.\]

Proporciona métodos estándar com para administrar elementos de datos de almacenamiento protegidos. El [**método PStoreCreateInstance**](pstorecreateinstance.md) devuelve un puntero a esta interfaz.

## <a name="members"></a>Miembros

La **interfaz IPStore** hereda de la [**interfaz IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IPStore** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IPStore** tiene estos métodos.



| Método                                                   | Descripción                                                                                                           |
|:---------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------|
| [**CloseItem**](ipstore-closeitem.md)                   | Cierra un elemento de datos especificado del almacenamiento protegido.<br/>                                                       |
| [**CreateSubtype**](ipstore-createsubtype.md)           | Crea el subtipo especificado dentro del tipo especificado.<br/>                                                   |
| [**Createtype**](ipstore-createtype.md)                 | Crea el tipo especificado con el nombre especificado.<br/>                                                        |
| [**DeleteItem**](ipstore-deleteitem.md)                 | Elimina el elemento especificado del almacenamiento protegido.<br/>                                                     |
| [**DeleteSubtype**](ipstore-deletesubtype.md)           | Elimina el subtipo de elemento especificado del almacenamiento protegido.<br/>                                             |
| [**DeleteType**](ipstore-deletetype.md)                 | Elimina el tipo especificado del almacenamiento protegido.<br/>                                                     |
| [**EnumItems**](ipstore-enumitems.md)                   | Devuelve el puntero de interfaz de un subtipo para enumerar elementos en la base de datos de almacenamiento protegida.<br/>        |
| [**EnumSubtypes**](ipstore-enumsubtypes.md)             | Devuelve una interfaz para enumerar subtipos de los tipos registrados actualmente en la base de datos protegida.<br/> |
| [**EnumTypes**](ipstore-enumtypes.md)                   | Devuelve una interfaz para enumerar los tipos registrados actualmente en la base de datos protegida.<br/>             |
| [**GetInfo**](ipstore-getinfo.md)                       | Recupera información sobre el proveedor de almacenamiento.<br/>                                                          |
| [**GetProvParam**](ipstore-getprovparam.md)             | Sin implementar.<br/>                                                                                           |
| [**GetSubtypeInfo**](ipstore-getsubtypeinfo.md)         | Recupera información asociada a un subtipo.<br/>                                                           |
| [**GetTypeInfo**](ipstore-gettypeinfo.md)               | Recupera información asociada a un tipo.<br/>                                                              |
| [**OpenItem**](ipstore-openitem.md)                     | Abre un elemento para varios accesos.<br/>                                                                       |
| [**ReadAccessRuleSet**](ipstore-readaccessruleset.md)   | Sin implementar.<br/>                                                                                           |
| [**ReadItem**](ipstore-readitem.md)                     | Lee el elemento de datos especificado del almacenamiento protegido.<br/>                                                      |
| [**SetProvParam**](ipstore-setprovparam.md)             | Establece la información del parámetro especificado.<br/>                                                                  |
| [**WriteAccessRuleset**](ipstore-writeaccessruleset.md) | Sin implementar.<br/>                                                                                           |
| [**WriteItem**](ipstore-writeitem.md)                   | Escribe un elemento de datos en el almacenamiento protegido.<br/>                                                                   |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Pstore.h</dt> </dl>    |
| Archivo DLL<br/>    | <dl> <dt>Pstorec.dll</dt> </dl> |



 

 
