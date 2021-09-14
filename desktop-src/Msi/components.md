---
description: El objeto Component representa una instancia única de un componente que está disponible para la enumeración.
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127158827"
---
# <a name="component-object"></a>Objeto de componente

El objeto Component representa una instancia única de un componente que está disponible para la enumeración.

**[Windows Installer 4.5 o versiones anteriores:](not-supported-in-windows-installer-4-5.md)** No se admite. Este objeto está disponible a partir de Windows Installer 5.0.

## <a name="members"></a>Members

El **objeto Component** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

El **objeto Component** tiene estas propiedades.



| Propiedad.                                                    | Descripción                                                                               |
|:------------------------------------------------------------|:------------------------------------------------------------------------------------------|
| [**ComponentCode**](component-componentcode.md)<br/> | Código de componente del componente en cuestión.<br/>                               |
| [**Contexto**](component-context.md)<br/>             | Contexto que se ha determinado que es aplicable al componente en cuestión.<br/> |
| [**UserSID**](component-usersid.md)<br/>             | SID de usuario para el componente enumerado.<br/>                                     |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 o posterior.<br/>                                         |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl> |
| IID<br/>     | IID IComponent se define como \_ 000C1097-0000-0000-C000-000000000046<br/>      |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Uso de la interfaz de Automation](using-the-automation-interface.md)
</dt> <dt>

[Windows Ejemplos de scripting del instalador](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




