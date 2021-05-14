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
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/12/2021
ms.locfileid: "109840656"
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
| [**Elemento**](folderitems-item.md)          | Recupera el [**objeto FolderItem**](folderitem.md) para un elemento especificado de la colección.<br/> |



 

### <a name="properties"></a>Propiedades

El **objeto FolderItems** tiene estas propiedades.



| Propiedad                                                  | Tipo de acceso          | Descripción                                                                                                   |
|:----------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------|
| [**Application**](folderitems-application.md)<br/> | Solo lectura<br/> | Contiene el [**objeto Application**](folderitems-application.md) de la colección de elementos de carpeta.<br/> |
| [**Contar**](folderitems-count.md)<br/>             | Solo lectura<br/> | Contiene el número de elementos de la colección.<br/>                                                    |
| [**Parent**](folderitems-parent.md)<br/>           | Solo lectura<br/> | Sin implementar.<br/>                                                                                   |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional, solo aplicaciones de escritorio de Windows \[ XP\]<br/>                                         |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                           |
| Encabezado<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                           |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                         |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll (versión 4.71 o posterior)</dt> </dl> |



 

 




