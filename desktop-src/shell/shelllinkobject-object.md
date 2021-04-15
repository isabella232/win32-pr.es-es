---
description: Administra vínculos de Shell. Este objeto hace que gran parte de la funcionalidad de la interfaz IShellLink esté disponible para las aplicaciones de scripting.
title: Objeto ShellLinkObject (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellLinkObject
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: d3c0ccf8-0f83-42f7-9d6f-1fb293da6364
ms.openlocfilehash: 1daf1aafae4bc230014890b79d4fb0310aa30a1f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104986026"
---
# <a name="shelllinkobject-object"></a>Objeto ShellLinkObject

Administra vínculos de Shell. Este objeto hace que gran parte de la funcionalidad de la interfaz [**IShellLink**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka) esté disponible para las aplicaciones de scripting.

## <a name="members"></a>Miembros

El objeto **ShellLinkObject** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

El objeto **ShellLinkObject** tiene estos métodos.



| Método                                                     | Descripción                                                                                    |
|:-----------------------------------------------------------|:-----------------------------------------------------------------------------------------------|
| [**GetIconLocation**](shelllinkobject-geticonlocation.md) | Obtiene la ubicación del icono asignado al vínculo.<br/>                                 |
| [**Resolver**](shelllinkobject-resolve.md)                 | Busca el destino de un vínculo de Shell, incluso si el destino se ha quitado o cambiado de nombre.<br/> |
| [**Guardar**](shelllinkobject-save.md)                       | Guarda todos los cambios realizados en el vínculo.<br/>                                                      |
| [**SetIconLocation**](shelllinkobject-seticonlocation.md) | Establece la ubicación del icono asignado al vínculo.<br/>                                 |



 

### <a name="properties"></a>Propiedades

El objeto **ShellLinkObject** tiene estas propiedades.



| Propiedad                                                                | Tipo de acceso           | Descripción                                                                                               |
|:------------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------|
| [**Argumentos**](shelllinkobject-arguments.md)<br/>               | Lectura/escritura<br/> | Contiene los argumentos de un vínculo.<br/>                                                                   |
| [**Descripción**](shelllinkobject-description.md)<br/>           | Lectura/escritura<br/> | Obtiene o establece la descripción del vínculo.<br/>                                                      |
| [**Tecla de acceso rápido**](shelllinkobject-hotkey.md)<br/>                     | Lectura/escritura<br/> | Obtiene o establece el método abreviado de teclado para el vínculo.<br/>                                               |
| [**Ruta**](shelllinkobject-path.md)<br/>                         | Lectura/escritura<br/> | Obtiene o establece la ruta de acceso al objeto de vínculo.<br/>                                                      |
| [**Información showcommand**](shelllinkobject-showcommand.md)<br/>           | Lectura/escritura<br/> | Obtiene o establece el estado de presentación inicial (con tamaño, minimizada o maximizada) del comando del vínculo.<br/> |
| [**WorkingDirectory**](shelllinkobject-workingdirectory.md)<br/> | Lectura/escritura<br/> | Obtiene o establece el directorio de trabajo especificado en el vínculo.<br/>                                      |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                          |
| IDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                        |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll (versión 5,0 o posterior)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Vínculos de Shell](./links.md)
</dt> </dl>

 

 
