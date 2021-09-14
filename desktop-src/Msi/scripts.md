---
description: Una acción personalizada puede llamar a funciones escritas en VBScript o JScript.
ms.assetid: d859713f-b8b8-4eb0-b678-52b5d880bd20
title: Scripts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 114a11c12e94dd2f3285757bd01167f14b412ac6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127274124"
---
# <a name="scripts"></a>Scripts

Una acción personalizada puede llamar a funciones escritas en VBScript o JScript. Windows El instalador no proporciona el motor de scripts. Por lo tanto, los autores que quieran usar un lenguaje de scripting durante la instalación deben asegurarse de que el motor de scripting adecuado esté disponible.

El instalador no admite JScript versión 1.0.

Una acción personalizada de 64 bits basada en scripts debe marcarse explícitamente como una acción personalizada de 64 bits agregando el bit **msidbCustomActionType64BitScript** al tipo numérico de acciones personalizadas en la columna Type de la [tabla CustomAction.](customaction-table.md) Para obtener información, [vea Acciones personalizadas de 64 bits.](64-bit-custom-actions.md)

Los siguientes tipos de acción personalizados básicos llaman a funciones escritas en script.



| Tipo de acción personalizada                                 | Descripción                                                                                    |
|----------------------------------------------------|------------------------------------------------------------------------------------------------|
| [Tipo de acción personalizada 5](custom-action-type-5.md)   | JScript archivo almacenado en una secuencia de tabla binaria.                                                  |
| [Tipo de acción personalizada 21](custom-action-type-21.md) | JScript archivo que se instala con un producto.                                                 |
| [Tipo de acción personalizada 53](custom-action-type-53.md) | JScript texto especificado por un valor de propiedad.                                                    |
| [Tipo de acción personalizada 37](custom-action-type-37.md) | JScript texto almacenado en la columna Destino de la [tabla CustomAction.](customaction-table.md)  |
| [Tipo de acción personalizada 6](custom-action-type-6.md)   | Archivo VBScript almacenado en una [secuencia de tabla](binary-table.md) binaria.                             |
| [Tipo de acción personalizada 22](custom-action-type-22.md) | Archivo VBScript que se instala con un producto.                                                |
| [Tipo de acción personalizada 54](custom-action-type-54.md) | Texto de VBScript especificado por un valor de propiedad.                                                   |
| [Tipo de acción personalizada 38](custom-action-type-38.md) | Texto de VBScript almacenado en la columna Destino de la [tabla CustomAction.](customaction-table.md) |



 

> [!Note]  
> El instalador ejecuta acciones personalizadas de script directamente y no usa el host Windows script. El **objeto WScript** no se puede usar dentro de una acción personalizada de script porque este objeto lo proporciona Windows host de script. Los objetos del modelo de objetos host de script de Windows solo se pueden usar en acciones personalizadas si el host de script de Windows está instalado en el equipo mediante la creación de nuevas instancias del objeto , con una llamada a CreateObject y proporcionando el ProgId del objeto (por ejemplo, "WScript.Shell"). Según el tipo de acción personalizada de script, se puede denegar el acceso a algunos objetos y métodos del modelo de objetos Windows Host de script por motivos de seguridad.

 

Para obtener más información, vea [Lista](summary-list-of-all-custom-action-types.md) de resumen de todos los tipos de acciones personalizadas para obtener un resumen de todos los tipos de acciones personalizadas y cómo se codifican en la [tabla CustomAction.](customaction-table.md)

 

 



