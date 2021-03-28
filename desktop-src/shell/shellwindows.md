---
description: Representa una colección de las ventanas abiertas que pertenecen al shell. Los métodos asociados a estos objetos pueden controlar y ejecutar comandos en el Shell y obtener otros objetos relacionados con el shell.
ms.assetid: cad1f961-7fb4-4ba1-be48-b664d3de2c60
title: Objeto ShellWindows (exdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellWindows
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 6a3a782dd4e29d56f5edc7a869004ac7b3fb7ccd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985566"
---
# <a name="shellwindows-object"></a>Objeto ShellWindows

Representa una colección de las ventanas abiertas que pertenecen al shell. Los métodos asociados a estos objetos pueden controlar y ejecutar comandos en el Shell y obtener otros objetos relacionados con el shell.

## <a name="members"></a>Miembros

El objeto **ShellWindows** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

El objeto **ShellWindows** tiene estos métodos.



| Método                                                 | Descripción                                                                                                         |
|:-------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------|
| [**\_NewEnum**](shellwindows--newenum-method-7ral.md) | Crea y devuelve un nuevo objeto **ShellWindows** que es una copia de este objeto **ShellWindows** .<br/>        |
| [**Elemento**](shellwindows-item.md)                      | Recupera un objeto [**InternetExplorer**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752084(v=vs.85)) que representa la ventana del shell.<br/> |



 

### <a name="properties"></a>Propiedades

El objeto **ShellWindows** tiene estas propiedades.



| Propiedad                                       | Tipo de acceso          | Descripción                                                |
|:-----------------------------------------------|:---------------------|:-----------------------------------------------------------|
| [**Count**](shellwindows-count.md)<br/> | Solo lectura<br/> | Contiene el número de elementos de la colección.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]<br/>                                         |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                           |
| Encabezado<br/>                   | <dl> <dt>Exdisp. h</dt> </dl>                            |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll (versión 4,71 o posterior)</dt> </dl> |



 

 
