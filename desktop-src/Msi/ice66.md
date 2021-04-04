---
description: ICE66 usa las tablas de la base de datos para determinar qué esquema debe usar la base de datos.
ms.assetid: 7cf929a0-2c4c-40ca-a902-dfd9dcd203b8
title: ICE66
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea1436ad791941c96c0484a02f40a60fc9939e73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810910"
---
# <a name="ice66"></a>ICE66

ICE66 usa las tablas de la base de datos para determinar qué esquema debe usar la base de datos.

Es posible que algunas funciones solo estén disponibles si el paquete está instalado en un sistema con una versión de Windows Installer actual.

## <a name="result"></a>Resultado

ICE66 publica una advertencia si la base de datos usa un esquema incorrecto.

## <a name="example"></a>Ejemplo

ICE66 notifica la siguiente advertencia para el ejemplo que se muestra.

``` syntax
WARNING: Complete functionality of the IsolatedComponents table is only available with Windows Installer versions 1.1 or greater. Your schema is 100.
```

Esta advertencia se puede omitir si desea que el paquete se instale con una versión de Windows Installer actual. Por ejemplo, si desea que el paquete se pueda instalar solo en la versión 2,0 o posterior, cambie el esquema del paquete (PID \_ PAGECOUNT) a 200.

[Tabla IsolatedComponent](isolatedcomponent-table.md)



| Componente \_ compartido | Aplicación de componentes \_ |
|-------------------|------------------------|
| Component1        | Component2             |



 

[Flujo de información de Resumen](summary-information-stream.md)



| PIDt           | Value |
|----------------|-------|
| PID \_ PAGECOUNT | 100   |



 

## <a name="table-used-during-execution"></a>Tabla utilizada durante la ejecución:

[\_Tabla de columnas](-columns-table.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 



