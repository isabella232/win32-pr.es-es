---
description: Representa una colección de objetos de extensión.
ms.assetid: b0d69df9-12c4-4872-b883-b029c4350502
title: Objeto NoticeNumbers
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NoticeNumbers
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 58d954fdeef66d6d0e5eadb3086cb549b59e5669
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690832"
---
# <a name="noticenumbers-object"></a>Objeto NoticeNumbers

\[El objeto **NoticeNumbers** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. Para obtener más información, vea [**calificador**](qualifier.md).\]

El objeto **NoticeNumbers** representa una colección de objetos de [**extensión**](extension.md) . Cada objeto de [**extensión**](extension.md) representa un número de aviso de usuario.

## <a name="when-to-use"></a>Cuándo se usa

El objeto **NoticeNumbers** se usa para realizar las siguientes tareas:

-   Recupera el número de objetos de [**extensión**](extension.md) de la colección.
-   Recupera un objeto de [**extensión**](extension.md) específico de la colección.
-   Recorrer en iteración la colección.

## <a name="members"></a>Miembros

El objeto **NoticeNumbers** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

El objeto **NoticeNumbers** tiene estas propiedades.



| Propiedad                                              | Tipo de acceso          | Descripción                                                                                                                                                                                                                     |
|:------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_NewEnum**](noticenumbers-newenum.md)<br/> | Solo lectura<br/> | Recupera una interfaz [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) en un objeto que se puede utilizar para enumerar la colección. Esta propiedad está oculta en Visual Basic Scripting Edition (VBScript).<br/> |
| [**Contabiliza**](noticenumbers-count.md)<br/>       | Solo lectura<br/> | Recupera el número de objetos de [**extensión**](extension.md) de la colección.<br/>                                                                                                                                    |
| [**Elemento**](noticenumbers-item.md)<br/>         | Solo lectura<br/> | Recupera el objeto de [**extensión**](extension.md) que representa el número de aviso indizado de la colección.<br/> Esta es la propiedad predeterminada.<br/>                                                            |



 

## <a name="remarks"></a>Observaciones

No se puede crear el objeto **NoticeNumbers** .

El objeto NoticeNumbers se usa en la propiedad [**Qualifier. NoticeNumbers**](qualifier-noticenumbers.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
