---
description: El objeto ComponentInfo representa los detalles adicionales sobre un componente que se puede obtener a través de una llamada de MsiGetComponentPathEx.
ms.assetid: 9b0ad0a1-c49f-4b14-817b-0cfc9b228d77
title: Objeto ComponentInfo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ComponentInfo
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 1890ff127f60188deae8fdad251e44b3edb614f7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653613"
---
# <a name="componentinfo-object"></a>Objeto ComponentInfo

El objeto ComponentInfo representa los detalles adicionales sobre un componente que se puede obtener a través de una llamada de MsiGetComponentPathEx.

**[Windows Installer 4,5 o una versión anterior](not-supported-in-windows-installer-4-5.md):** No compatible. Este objeto está disponible a partir de Windows Installer 5,0.

## <a name="members"></a>Miembros

El objeto **ComponentInfo** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

El objeto **ComponentInfo** tiene estas propiedades.



| Propiedad                                                        | Descripción                                                 |
|:----------------------------------------------------------------|:------------------------------------------------------------|
| [**ComponentCode**](componentinfo-componentcode.md)<br/> | Código de componente del componente en cuestión.<br/> |
| [**Ruta**](componentinfo-componentcode.md)<br/>          | Ruta de acceso del componente.<br/>                       |
| [**State**](componentinfo-state.md)<br/>                 | Estado del componente.<br/>                      |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 o posterior.<br/>                                         |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl> |
| IID<br/>     | IID \_ IComponentInfo se define como 000C1099-0000-0000-C000-000000000046<br/>  |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Usar la interfaz de automatización](using-the-automation-interface.md)
</dt> <dt>

[Ejemplos de scripting Windows Installer](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




