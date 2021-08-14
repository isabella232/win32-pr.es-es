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
ms.openlocfilehash: a59aa1d9f7bdc5babc29461ca90c01b6fe604482cb78ba6549e782b1e34d54b5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119252005"
---
# <a name="componentinfo-object"></a>Objeto ComponentInfo

El objeto ComponentInfo representa detalles adicionales sobre un componente que se pueden obtener a través de una llamada desde MsiGetComponentPathEx.

**[Windows Instalador 4.5 o anterior:](not-supported-in-windows-installer-4-5.md)** No se admite. Este objeto está disponible a partir de Windows Installer 5.0.

## <a name="members"></a>Miembros

El **objeto ComponentInfo** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

El **objeto ComponentInfo** tiene estas propiedades.



| Propiedad                                                        | Descripción                                                 |
|:----------------------------------------------------------------|:------------------------------------------------------------|
| [**ComponentCode**](componentinfo-componentcode.md)<br/> | Código de componente del componente en cuestión.<br/> |
| [**Path**](componentinfo-componentcode.md)<br/>          | Ruta de acceso del componente.<br/>                       |
| [**Estado**](componentinfo-state.md)<br/>                 | Estado del componente.<br/>                      |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 o posterior.<br/>                                         |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl> |
| IID<br/>     | IID IComponentInfo se define como \_ 000C1099-0000-0000-C000-00000000046<br/>  |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Uso de la interfaz de Automation](using-the-automation-interface.md)
</dt> <dt>

[Windows Ejemplos de scripting del instalador](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




