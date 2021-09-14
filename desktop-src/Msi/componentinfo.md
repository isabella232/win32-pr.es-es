---
description: El objeto ComponentInfo representa detalles adicionales sobre un componente que se pueden obtener a través de una llamada desde MsiGetComponentPathEx.
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127158829"
---
# <a name="componentinfo-object"></a>Objeto ComponentInfo

El objeto ComponentInfo representa detalles adicionales sobre un componente que se pueden obtener a través de una llamada desde MsiGetComponentPathEx.

**[Windows instalador 4.5 o anterior:](not-supported-in-windows-installer-4-5.md)** No se admite. Este objeto está disponible a partir de Windows Installer 5.0.

## <a name="members"></a>Members

El **objeto ComponentInfo** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

El **objeto ComponentInfo** tiene estas propiedades.



| Propiedad.                                                        | Descripción                                                 |
|:----------------------------------------------------------------|:------------------------------------------------------------|
| [**ComponentCode**](componentinfo-componentcode.md)<br/> | Código de componente del componente en cuestión.<br/> |
| [**Camino**](componentinfo-componentcode.md)<br/>          | Ruta de acceso del componente.<br/>                       |
| [**Estado**](componentinfo-state.md)<br/>                 | Estado del componente.<br/>                      |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 o posterior.<br/>                                         |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl> |
| IID<br/>     | IID IComponentInfo se define como \_ 000C1099-0000-0000-C000-00000000046<br/>  |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Uso de la interfaz de Automation](using-the-automation-interface.md)
</dt> <dt>

[Windows Ejemplos de scripting del instalador](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




