---
description: El objeto de cliente representa una relación entre un componente de y un producto de cliente.
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
ms.openlocfilehash: 75cb21a4149d8e6758ab24796949777b8052b120
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670894"
---
# <a name="client-object"></a>Objeto de cliente

El objeto de cliente representa una relación entre un componente de y un producto de cliente.

**[Windows Installer 4,5 o una versión anterior](not-supported-in-windows-installer-4-5.md):** No compatible. Este objeto está disponible a partir de Windows Installer 5,0.

## <a name="members"></a>Miembros

El objeto de **cliente** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

El objeto de **cliente** tiene estas propiedades.



| Propiedad                                                 | Descripción                                                 |
|:---------------------------------------------------------|:------------------------------------------------------------|
| [**ComponentCode**](client-componentcode.md)<br/> | Código de componente del componente en cuestión.<br/> |
| [**Context**](client-context.md)<br/>             | Contexto del producto.<br/>                      |
| [**ProductCode**](client-productcode.md)<br/>     | Producto de cliente del componente en cuestión.<br/> |
| [**UserSID**](client-usersid.md)<br/>             | SID de usuario del componente.<br/>                  |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 o posterior.<br/>                                         |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl> |
| IID<br/>     | IID \_ IClient se define como 000C1098-0000-0000-C000-000000000046<br/>         |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Usar la interfaz de automatización](using-the-automation-interface.md)
</dt> <dt>

[Ejemplos de scripting Windows Installer](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




