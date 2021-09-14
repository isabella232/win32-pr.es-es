---
description: Representa una carpeta shell. Este objeto contiene propiedades y métodos que permiten recuperar información sobre la carpeta.
ms.assetid: f1e82c61-205e-47c8-bc7c-6a52410a672e
title: Objeto Folder (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Folder
api_type:
- COM
api_location:
- Shldisp.h
ms.openlocfilehash: d37966b13a182161c1a6248c93eabaf5dfa3597c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127363139"
---
# <a name="folder-object"></a>Objeto Folder

Representa una carpeta shell. Este objeto contiene propiedades y métodos que permiten recuperar información sobre la carpeta.

## <a name="members"></a>Members

El **objeto Folder** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

El **objeto Folder** tiene estos métodos.



| Método                                      | Descripción                                                                                                                |
|:--------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------|
| [**CopyHere**](folder-copyhere.md)         | Copia un elemento o elementos en una carpeta.<br/>                                                                            |
| [**GetDetailsOf**](folder-getdetailsof.md) | Recupera detalles sobre un elemento de una carpeta. Por ejemplo, su tamaño, tipo o la hora de su última modificación.<br/> |
| [**Elementos**](folder-items.md)               | Recupera un [**objeto FolderItems**](folderitems.md) que representa la colección de elementos de la carpeta .<br/>    |
| [**MoveHere**](folder-movehere.md)         | Mueve un elemento o elementos a esta carpeta.<br/>                                                                          |
| [**NewFolder**](folder-newfolder.md)       | Crea una nueva carpeta.<br/>                                                                                           |
| [**ParseName**](folder-parsename.md)       | Crea y devuelve un [**objeto FolderItem**](folderitem.md) que representa un elemento especificado.<br/>                 |



 

### <a name="properties"></a>Propiedades

El **objeto Folder** tiene estas propiedades.



| Propiedad.                                               | Tipo de acceso          | Descripción                                          |
|:-------------------------------------------------------|:---------------------|:-----------------------------------------------------|
| [**Application**](folder-application.md)<br/>   | Solo lectura<br/> | Contiene el objeto Application de la carpeta.<br/> |
| [**Parent**](folder-parent.md)<br/>             | Solo lectura<br/> | Sin implementar.<br/>                          |
| [**ParentFolder**](folder-parentfolder.md)<br/> | Solo lectura<br/> | Contiene el objeto **Folder** primario.<br/>    |
| [**Título**](folder-title.md)<br/>               | Solo lectura<br/> | Contiene el título de la carpeta.<br/>         |



 

## <a name="remarks"></a>Observaciones

> [!Note]  
> No todos los métodos se implementan para todas las carpetas. Por ejemplo, el [**método ParseName**](folder-parsename.md) no se implementa para la carpeta Panel de control (CSIDL \_ CONTROLS). Si intenta llamar a un método sin implementar, se genera un error 0x800A01BD (decimal 445).

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional, Windows aplicaciones de escritorio XP \[\]<br/>                 |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                   |
| Encabezado<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl> |



 

 




