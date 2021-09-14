---
description: El orden de ejecución de la acción viene determinado por la secuencia de acciones que se han creado en las tablas de secuencia y por el orden en que el instalador ejecuta las tablas de secuencia.
ms.assetid: f4666f49-4ea1-42fb-b32d-ce77de79b212
title: Orden de ejecución de la acción
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 954c44f6e2525deb3375cb9ea72d0320df3a5f02
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159238"
---
# <a name="action-execution-order"></a>Orden de ejecución de la acción

El orden de ejecución de la acción viene determinado por [](s-gly.md) la secuencia de acciones que se han creado en las tablas de secuencia y por el orden en que el instalador ejecuta las tablas de secuencia. Para obtener más información, vea las secuencias de acciones sugeridas en [Uso de una tabla de secuencias](using-a-sequence-table.md).

El instalador ejecuta tablas de secuencia en respuesta a una solicitud de instalación, [anuncio](advertisement.md)o [una instalación administrativa.](administrative-installation.md) Por ejemplo, en respuesta al uso de las opciones de línea de comandos /I, /J o [/A](command-line-options.md), no se llama a las acciones [INSTALL](install-action.md), [ADVERTISE](advertise-action.md)y [ADMIN](admin-action.md) desde dentro de la secuencia de acciones. En su lugar, estas acciones de alto nivel se pasan al instalador cuando se inicializa el instalador.

Si se pasa al instalador la acción INSTALL y el paquete de instalación se ha escrito con una interfaz de usuario, el instalador ejecuta primero las acciones en la tabla [InstallUISequence](installuisequence-table.md) y, a continuación, ejecuta las acciones en la tabla [InstallExecuteSequence](installexecutesequence-table.md) en orden. Si el paquete no tiene ninguna interfaz de usuario, el instalador ejecuta las acciones de la tabla InstallExecuteSequence en orden.

Si se pasa al instalador la acción ADMIN y el paquete de instalación se ha escrito con una interfaz de usuario, el instalador ejecuta primero la tabla [AdminUISequence](adminuisequence-table.md) y, a continuación, ejecuta la tabla [AdminExecuteSequence](adminexecutesequence-table.md). Si el paquete no tiene ninguna interfaz de usuario, el instalador ejecuta la tabla AdminExecute.

Si se pasa al instalador la acción ADVERTISE, el instalador ejecuta la [tabla AdvtExecuteSequence.](advtexecutesequence-table.md)

> [!Note]  
> El instalador no usa la [tabla AdvtUISequence.](advtuisequence-table.md) La tabla AdvtUISequence no debe existir en la base de datos de instalación o debe quedar vacía.

 

Cuando el instalador ejecuta una tabla de secuencias, ejecuta acciones en el orden de los números de secuencia enumerados en la columna Secuencia. El orden de acción siempre es lineal sin bifurcación ni bucle. Los desarrolladores de paquetes pueden impedir condicionalmente que se ejecute una acción determinada mediante la creación de una expresión lógica en la columna Condición . El instalador omite la acción cada vez que la condición se evalúa como False. Vea [Usar una tabla de secuencia y](using-a-sequence-table.md) [sintaxis de instrucción condicional.](conditional-statement-syntax.md)

Todas las tablas de secuencia tienen las siguientes columnas.



| Columna    | Descripción                                                                                                                                                                                                                                   |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Acción    | Clave principal de la tabla; el nombre de la acción debe ser único.                                                                                                                                                                                |
| Condición | Expresión booleana que se usa para determinar si se va a realizar la acción. La acción se ejecuta si este campo está en blanco o contiene una expresión que se evalúa como True. La acción no se ejecuta si la expresión se evalúa como False. |
| Secuencia  | Número de secuencia relativa utilizado para determinar el orden en el que se ejecutan las acciones.                                                                                                                                                         |



 

 

 



