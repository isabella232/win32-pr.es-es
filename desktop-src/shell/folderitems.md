---
description: Representa la colección de elementos de una carpeta de Shell. Este objeto contiene propiedades y métodos que permiten recuperar información sobre la colección.
title: Objeto FolderItems (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItems
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: b99201b3-95e8-4ddd-b338-dee8d107d0a0
ms.openlocfilehash: 2b6e9506d6c2354018a41ae7a15ca6e8e1900857
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127468219"
---
# <a name="folderitems-object"></a>Objeto FolderItems

Representa la colección de elementos de una carpeta de Shell. Este objeto contiene propiedades y métodos que permiten recuperar información sobre la colección.

## <a name="members"></a>Members

El **objeto FolderItems** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

El **objeto FolderItems** tiene estos métodos.



| Método                                    | Descripción                                                                                              |
|:------------------------------------------|:---------------------------------------------------------------------------------------------------------|
| [**\_NewEnum**](folderitems--newenum.md) | Sin implementar.<br/>                                                                              |
| [**Artículo**](folderitems-item.md)          | Recupera el [**objeto FolderItem**](folderitem.md) para un elemento especificado de la colección.<br/> |



 

### <a name="properties"></a>Propiedades

El **objeto FolderItems** tiene estas propiedades.



| Propiedad.                                                  | Tipo de acceso          | Descripción                                                                                                   |
|:----------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------|
| [**Application**](folderitems-application.md)<br/> | Solo lectura<br/> | Contiene el [**objeto Application**](folderitems-application.md) de la colección de elementos de carpeta.<br/> |
| [**Count**](folderitems-count.md)<br/>             | Solo lectura<br/> | Contiene el número de elementos de la colección.<br/>                                                    |
| [**Parent**](folderitems-parent.md)<br/>           | Solo lectura<br/> | Sin implementar.<br/>                                                                                   |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional, Windows solo aplicaciones \[ de escritorio XP\]<br/>                                         |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                           |
| Encabezado<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                           |
| IDL<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                         |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll (versión 4.71 o posterior)</dt> </dl> |



 

 




