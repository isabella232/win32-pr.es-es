---
description: 'Objeto NoticeNumbers: representa una colección de objetos Extension.'
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
ms.openlocfilehash: b2bd6e653eabe9b25588fd29517ac94e0c878fdb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090763"
---
# <a name="noticenumbers-object"></a>Objeto NoticeNumbers

\[El **objeto NoticeNumbers** está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. Para obtener más información, vea [**Calificador**](qualifier.md).\]

El **objeto NoticeNumbers** representa una colección de [**objetos Extension.**](extension.md) Cada [**objeto Extension**](extension.md) representa un número de aviso de usuario.

## <a name="when-to-use"></a>Cuándo se usa

El **objeto NoticeNumbers** se usa para realizar las siguientes tareas:

-   Recupere el número de [**objetos Extension**](extension.md) de la colección.
-   Recuperar un objeto [**Extension**](extension.md) específico de la colección.
-   Recorrer en iteración la colección.

## <a name="members"></a>Miembros

El **objeto NoticeNumbers** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

El **objeto NoticeNumbers** tiene estas propiedades.



| Propiedad                                              | Tipo de acceso          | Descripción                                                                                                                                                                                                                     |
|:------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_NewEnum**](noticenumbers-newenum.md)<br/> | Solo lectura<br/> | Recupera una [**interfaz IEnumVARIANT en**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) un objeto que se puede usar para enumerar la colección. Esta propiedad está oculta en Visual Basic Scripting Edition (VBScript).<br/> |
| [**Contar**](noticenumbers-count.md)<br/>       | Solo lectura<br/> | Recupera el número de [**objetos Extension**](extension.md) de la colección.<br/>                                                                                                                                    |
| [**Elemento**](noticenumbers-item.md)<br/>         | Solo lectura<br/> | Recupera el objeto [**Extension**](extension.md) que representa el número de aviso indexado de la colección.<br/> Esta es la propiedad predeterminada.<br/>                                                            |



 

## <a name="remarks"></a>Comentarios

No se puede crear el objeto **NoticeNumbers.**

El objeto NoticeNumbers se usa en la [**propiedad Qualifier.NoticeNumbers.**](qualifier-noticenumbers.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
