---
description: Para cada contraseña que debe escribir el usuario, agregue un control de edición en un cuadro de diálogo que almacene el valor de la contraseña en una propiedad.
ms.assetid: aa4ff8b8-cbbb-4b18-83b3-279e52d9f6d3
title: Crear la interfaz de usuario para la entrada de contraseña
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b37cd7bb9531cbf63a443011656f200717dc0214
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667026"
---
# <a name="authoring-the-user-interface-for-password-input"></a>Crear la interfaz de usuario para la entrada de contraseña

Para cada contraseña que debe escribir el usuario, agregue un control de edición en un cuadro de diálogo que almacene el valor de la contraseña en una propiedad. Este [control de edición](edit-control.md) debe tener el [atributo de control de contraseña](password-control-attribute.md). Esto especifica que la propiedad especificada es una contraseña e impide que el instalador escriba la propiedad en el archivo de registro.

Los [atributos de control](control-attributes.md) del control de edición de contraseña son MsidbControlAttributesVisible, MsidbControlAttributesEnabled y msidbControlAttributesPasswordInput (1 + 2 + 2097152). Los valores X, Y, ancho, alto y control \_ siguiente dependen del diseño del control en el cuadro de diálogo.

[Tabla de control](control-table.md)



| Diálogo\_ | control\_            | Tipo | X   | Y   | Ancho | Alto | Atributos | Propiedad         | Texto | Control \_ siguiente | Ayuda |
|----------|----------------------|------|-----|-----|-------|--------|------------|------------------|------|---------------|------|
| Cuadro de diálogo | TestUserPasswordEdit | Editar | 25  | 120 | 300   | 20     | 2097155    | TESTUSERPASSWORD |      | Cancelar        |      |



 

Continúe con [la protección de la instalación](securing-the-installation.md).

 

 



