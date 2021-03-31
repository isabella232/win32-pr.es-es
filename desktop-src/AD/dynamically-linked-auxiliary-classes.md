---
title: Clases auxiliares vinculadas dinámicamente
description: Una clase auxiliar vinculada dinámicamente es una clase que se adjunta a un objeto individual, en lugar de a una clase de objeto.
ms.assetid: 10530a3c-89fc-4ff0-a0b7-1c9a27659003
ms.tgt_platform: multiple
keywords:
- Clases auxiliares vinculadas dinámicamente AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd0cacb09d3aef05bcaf0ef729411c2e023469be
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268291"
---
# <a name="dynamically-linked-auxiliary-classes"></a>Clases auxiliares vinculadas dinámicamente

Una clase auxiliar vinculada dinámicamente es una clase que se adjunta a un objeto individual, en lugar de a una clase de objeto. La vinculación dinámica permite almacenar atributos adicionales con un objeto individual sin el impacto en todo el bosque de la extensión de la definición de esquema de una clase completa. Por ejemplo, una empresa puede usar la vinculación dinámica para asociar una clase auxiliar específica de ventas a los objetos de usuario de sus vendedores y otras clases auxiliares específicas del Departamento a los objetos de usuario de los empleados de otros departamentos.

La vinculación dinámica no es compleja: agregue el nombre de la clase auxiliar a los valores del atributo **objectClass** de un objeto. Si la clase auxiliar tiene atributos obligatorios (**mustHave** o **systemMustHave**), debe establecerlos al mismo tiempo. Para obtener más información y un ejemplo de código, vea [Agregar una clase auxiliar a una instancia de objeto](adding-an-auxiliary-class-to-an-object-instance.md).

Para quitar una clase auxiliar vinculada dinámicamente, borre los valores de todos los atributos de la clase auxiliar y, a continuación, quite el nombre de la clase auxiliar del atributo **objectClass** del objeto.

Si agrega dinámicamente una clase auxiliar que es una subclase de otra clase auxiliar, ambas clases auxiliares se agregan al objeto de destino. Sin embargo, al quitar la clase auxiliar secundaria no se quita su elemento primario; cada clase se debe quitar explícitamente.

 

 




