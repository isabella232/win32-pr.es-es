---
description: Para cada contraseña que debe especificar el usuario, agregue un control de edición en un cuadro de diálogo que almacena el valor de la contraseña en una propiedad .
ms.assetid: aa4ff8b8-cbbb-4b18-83b3-279e52d9f6d3
title: Creación de la Interfaz de usuario para la entrada de contraseña
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b558243e24e4977d8e28311ac7643c118a26cdf62c89366694a16227b30c1969
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119066075"
---
# <a name="authoring-the-user-interface-for-password-input"></a>Creación de la Interfaz de usuario para la entrada de contraseña

Para cada contraseña que debe especificar el usuario, agregue un control de edición en un cuadro de diálogo que almacena el valor de la contraseña en una propiedad . Este [control de edición](edit-control.md) debe tener el atributo [de control de contraseña](password-control-attribute.md). Esto especifica que la propiedad especificada es una contraseña e impide que el instalador escriba la propiedad en el archivo de registro.

Los [atributos de control](control-attributes.md) para el control de edición de contraseñas son msidbControlAttributesVisible, msidbControlAttributesEnabled y msidbControlAttributesPasswordInput (1 + 2 + 2097152). X, Y, Width, Height y Control Next dependen del \_ diseño del control en el cuadro de diálogo.

[Tabla de controles](control-table.md)



| Diálogo\_ | control\_            | Tipo | X   | Y   | Ancho | Alto | Atributos | Propiedad         | Texto | Control \_ Siguiente | Ayuda |
|----------|----------------------|------|-----|-----|-------|--------|------------|------------------|------|---------------|------|
| MyDialog | TestUserPasswordEdit | Editar | 25  | 120 | 300   | 20     | 2097155    | TESTUSERPASSWORD |      | Cancelar        |      |



 

Continúe con [La protección de la instalación](securing-the-installation.md).

 

 



