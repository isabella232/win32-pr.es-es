---
description: Para cada contraseña que debe especificar el usuario, agregue un control de edición en un cuadro de diálogo que almacena el valor de la contraseña en una propiedad .
ms.assetid: aa4ff8b8-cbbb-4b18-83b3-279e52d9f6d3
title: Creación de la Interfaz de usuario para la entrada de contraseña
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b37cd7bb9531cbf63a443011656f200717dc0214
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159008"
---
# <a name="authoring-the-user-interface-for-password-input"></a>Creación de la Interfaz de usuario para la entrada de contraseña

Para cada contraseña que debe especificar el usuario, agregue un control de edición en un cuadro de diálogo que almacena el valor de la contraseña en una propiedad . Este [control de edición](edit-control.md) debe tener el [atributo de control de contraseña](password-control-attribute.md). Esto especifica que la propiedad especificada es una contraseña e impide que el instalador escriba la propiedad en el archivo de registro.

Los [atributos de control](control-attributes.md) para el control de edición de contraseñas son msidbControlAttributesVisible, msidbControlAttributesEnabled y msidbControlAttributesPasswordInput (1 + 2 + 2097152). X, Y, Width, Height y Control \_ Next dependen del diseño del control en el cuadro de diálogo.

[Tabla de control](control-table.md)



| Diálogo\_ | control\_            | Tipo | X   | Y   | Ancho | Alto | Atributos | Propiedad.         | Texto | Control \_ Siguiente | Ayuda |
|----------|----------------------|------|-----|-----|-------|--------|------------|------------------|------|---------------|------|
| MyDialog | TestUserPasswordEdit | Editar | 25  | 120 | 300   | 20     | 2097155    | TESTUSERPASSWORD |      | Cancelar        |      |



 

Continúe con [Protección de la instalación.](securing-the-installation.md)

 

 



