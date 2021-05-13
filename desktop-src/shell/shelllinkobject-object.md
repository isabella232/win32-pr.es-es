---
description: Administra los vínculos de Shell. Este objeto hace que gran parte de la funcionalidad de la interfaz IShellLink esté disponible para las aplicaciones de scripting.
title: Objeto ShellLinkObject (Shldisp.h)
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
ms.openlocfilehash: 5862ae3c9b7bf1262edbc28b06f2963f2e577275
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842636"
---
# <a name="shelllinkobject-object"></a>Objeto ShellLinkObject

Administra los vínculos de Shell. Este objeto hace que gran parte de la funcionalidad de la [**interfaz IShellLink**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka) esté disponible para las aplicaciones de scripting.

## <a name="members"></a>Members

El **objeto ShellLinkObject** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

El **objeto ShellLinkObject** tiene estos métodos.



| Método                                                     | Descripción                                                                                    |
|:-----------------------------------------------------------|:-----------------------------------------------------------------------------------------------|
| [**GetIconLocation**](shelllinkobject-geticonlocation.md) | Obtiene la ubicación del icono asignado al vínculo.<br/>                                 |
| [**Resolver**](shelllinkobject-resolve.md)                 | Busca el destino de un vínculo de Shell, incluso si se ha movido o cambiado el nombre del destino.<br/> |
| [**Guardar**](shelllinkobject-save.md)                       | Guarda todos los cambios en el vínculo.<br/>                                                      |
| [**SetIconLocation**](shelllinkobject-seticonlocation.md) | Establece la ubicación del icono asignado al vínculo.<br/>                                 |



 

### <a name="properties"></a>Propiedades

El **objeto ShellLinkObject** tiene estas propiedades.



| Propiedad                                                                | Tipo de acceso           | Descripción                                                                                               |
|:------------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------|
| [**Argumentos**](shelllinkobject-arguments.md)<br/>               | Lectura y escritura<br/> | Contiene los argumentos de un vínculo.<br/>                                                                   |
| [**Descripción**](shelllinkobject-description.md)<br/>           | Lectura y escritura<br/> | Obtiene o establece la descripción del vínculo.<br/>                                                      |
| [**Tecla de acceso rápido**](shelllinkobject-hotkey.md)<br/>                     | Lectura y escritura<br/> | Obtiene o establece el método abreviado de teclado para el vínculo.<br/>                                               |
| [**Camino**](shelllinkobject-path.md)<br/>                         | Lectura y escritura<br/> | Obtiene o establece la ruta de acceso al objeto de vínculo.<br/>                                                      |
| [**ShowCommand**](shelllinkobject-showcommand.md)<br/>           | Lectura y escritura<br/> | Obtiene o establece el estado de presentación inicial (tamaño, minimizado o maximizado) del comando del vínculo.<br/> |
| [**WorkingDirectory**](shelllinkobject-workingdirectory.md)<br/> | Lectura y escritura<br/> | Obtiene o establece el directorio de trabajo especificado en el vínculo.<br/>                                      |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional, solo aplicaciones de escritorio de Windows \[ XP\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                          |
| Header<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                          |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                        |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll (versión 5.0 o posterior)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Vínculos de shell](./links.md)
</dt> </dl>

 

 
