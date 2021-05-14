---
description: Representa la colección de verbos para un elemento de una carpeta de Shell. Este objeto contiene propiedades y métodos que permiten recuperar información sobre la colección.
title: Objeto FolderItemVerbs (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItemVerbs
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 31badb4b-b89e-4294-9dd7-bda716e163b2
ms.openlocfilehash: 8206c2113e2fa60abef41e43e4739b6eefd77dd4
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/12/2021
ms.locfileid: "109840616"
---
# <a name="folderitemverbs-object"></a>Objeto FolderItemVerbs

Representa la colección de verbos para un elemento de una carpeta de Shell. Este objeto contiene propiedades y métodos que permiten recuperar información sobre la colección.

## <a name="members"></a>Members

El **objeto FolderItemVerbs** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

El **objeto FolderItemVerbs** tiene estos métodos.



| Método                                        | Descripción                                                                                                      |
|:----------------------------------------------|:-----------------------------------------------------------------------------------------------------------------|
| [**\_NewEnum**](folderitemverbs--newenum.md) | Crea y devuelve un **nuevo objeto FolderItemVerbs** que es una copia de este objeto FolderItemVerbs.<br/>   |
| [**Elemento**](folderitemverbs-item.md)          | Recupera el [**objeto FolderItemVerb**](folderitemverb.md) para un elemento especificado de la colección.<br/> |



 

### <a name="properties"></a>Propiedades

El **objeto FolderItemVerbs** tiene estas propiedades.



| Propiedad                                                      | Tipo de acceso          | Descripción                                                |
|:--------------------------------------------------------------|:---------------------|:-----------------------------------------------------------|
| [**Application**](folderitemverbs-application.md)<br/> | Solo lectura<br/> | Sin implementar.<br/>                                |
| [**Contar**](folderitemverbs-count.md)<br/>             | Solo lectura<br/> | Contiene el número de elementos de la colección.<br/> |
| [**Parent**](folderitemverbs-parent.md)<br/>           | Solo lectura<br/> | Sin implementar.<br/>                                |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional, solo aplicaciones de escritorio de Windows \[ XP\]<br/>                                         |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                           |
| Encabezado<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                           |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                         |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll (versión 4.71 o posterior)</dt> </dl> |



 

 




