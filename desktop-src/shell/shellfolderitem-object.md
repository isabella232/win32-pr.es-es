---
description: Extiende el objeto FolderItem. Además de las propiedades y los métodos admitidos por FolderItem, ShellFolderItem tiene dos métodos adicionales.
title: Objeto ShellFolderItem (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellFolderItem
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 0e2f4c91-f9f9-4daa-a801-9c7fea8af738
ms.openlocfilehash: a9e6d6b3f954f0c8ee4b13fb651a9ea04274deb6
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/12/2021
ms.locfileid: "109840776"
---
# <a name="shellfolderitem-object"></a>Objeto ShellFolderItem

Extiende el [**objeto FolderItem.**](folderitem.md) Además de las propiedades y los métodos admitidos **por FolderItem,** **ShellFolderItem** tiene dos métodos adicionales.

## <a name="members"></a>Members

El **objeto ShellFolderItem** tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

El **objeto ShellFolderItem** tiene estos métodos.



| Método                                                       | Descripción                                                                                                                                                                                         |
|:-------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ExtendedProperty**](shellfolderitem-extendedproperty.md) | Obtiene el valor de una propiedad del conjunto de propiedades de un elemento. La propiedad se puede especificar por nombre o por el identificador de formato (FMTID) y el identificador de propiedad (PID) del conjunto de propiedades.<br/> |
| [**InvokeVerbEx**](invokeverbex.md)                         | Ejecuta un verbo en un elemento de Shell.<br/>                                                                                                                                                         |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                    |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                          |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                        |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll (versión 5.0 o posterior)</dt> </dl> |



 

 




