---
description: El objeto de componente representa una instancia única de un componente que está disponible para la enumeración.
ms.assetid: cdc99bc3-9e2a-49db-8c01-b9634aefac38
title: Objeto de componente
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Component
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 5e31d6a7c3d2422111d0d8c3247e022fa35bdc43
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653612"
---
# <a name="component-object"></a>Objeto de componente

El objeto de componente representa una instancia única de un componente que está disponible para la enumeración.

**[Windows Installer 4,5 o una versión anterior](not-supported-in-windows-installer-4-5.md):** No compatible. Este objeto está disponible a partir de Windows Installer 5,0.

## <a name="members"></a>Miembros

El objeto de **componente** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

El objeto de **componente** tiene estas propiedades.



| Propiedad                                                    | Descripción                                                                               |
|:------------------------------------------------------------|:------------------------------------------------------------------------------------------|
| [**ComponentCode**](component-componentcode.md)<br/> | Código de componente del componente en cuestión.<br/>                               |
| [**Context**](component-context.md)<br/>             | Contexto que se ha determinado que es aplicable al componente en cuestión.<br/> |
| [**UserSID**](component-usersid.md)<br/>             | SID de usuario para el componente enumerado.<br/>                                     |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 o posterior.<br/>                                         |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl> |
| IID<br/>     | IID \_ IComponent se define como 000C1097-0000-0000-C000-000000000046<br/>      |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Usar la interfaz de automatización](using-the-automation-interface.md)
</dt> <dt>

[Ejemplos de scripting Windows Installer](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




