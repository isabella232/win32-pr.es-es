---
description: El objeto Client representa una relación entre un componente y un producto cliente.
ms.assetid: ac1fbd74-fbc4-4f76-8e14-af48443a8528
title: Objeto de cliente
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Client
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 4308084bb1e5e081668bbe85dfb458f747fe34b25be0dd1858b5a7b7fae8a269
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119328385"
---
# <a name="client-object"></a>Objeto de cliente

El objeto Client representa una relación entre un componente y un producto cliente.

**[Windows Instalador 4.5 o anterior:](not-supported-in-windows-installer-4-5.md)** No se admite. Este objeto está disponible a partir de Windows Installer 5.0.

## <a name="members"></a>Miembros

El **objeto** Client tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

El **objeto** Client tiene estas propiedades.



| Propiedad                                                 | Descripción                                                 |
|:---------------------------------------------------------|:------------------------------------------------------------|
| [**ComponentCode**](client-componentcode.md)<br/> | Código de componente del componente en cuestión.<br/> |
| [**Contexto**](client-context.md)<br/>             | Contexto del producto.<br/>                      |
| [**ProductCode**](client-productcode.md)<br/>     | Producto cliente del componente en cuestión.<br/> |
| [**UserSID**](client-usersid.md)<br/>             | SID de usuario para el componente.<br/>                  |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 o posterior.<br/>                                         |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl> |
| IID<br/>     | IID IClient se define como \_ 000C1098-0000-0000-C000-00000000046<br/>         |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Uso de la interfaz de Automation](using-the-automation-interface.md)
</dt> <dt>

[Windows Ejemplos de scripting del instalador](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




