---
description: ICE66 usa las tablas de la base de datos para determinar qué esquema debe usar la base de datos.
ms.assetid: 7cf929a0-2c4c-40ca-a902-dfd9dcd203b8
title: ICE66
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 023450a451a412c47c21904ab96a13e4513c71f8327966dffa5b657b1b65bb65
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119787405"
---
# <a name="ice66"></a>ICE66

ICE66 usa las tablas de la base de datos para determinar qué esquema debe usar la base de datos.

Es posible que algunas funcionalidades solo estén disponibles si el paquete está instalado en un sistema con una versión Windows instalador actual.

## <a name="result"></a>Resultado

ICE66 envía una advertencia si la base de datos usa un esquema incorrecto.

## <a name="example"></a>Ejemplo

ICE66 notifica la advertencia siguiente para el ejemplo mostrado.

``` syntax
WARNING: Complete functionality of the IsolatedComponents table is only available with Windows Installer versions 1.1 or greater. Your schema is 100.
```

Esta advertencia se puede omitir si desea que el paquete se instale con una versión Windows instalador actual. Por ejemplo, si desea que el paquete solo se pueda instalar en la versión 2.0 o posterior, cambie el esquema del paquete (PID \_ PAGECOUNT) a 200.

[Tabla IsolatedComponent](isolatedcomponent-table.md)



| Componente \_ compartido | Aplicación \_ de componentes |
|-------------------|------------------------|
| Componente1        | Componente 2             |



 

[Secuencia de información de resumen](summary-information-stream.md)



| PIDt           | Valor |
|----------------|-------|
| PID \_ PAGECOUNT | 100   |



 

## <a name="table-used-during-execution"></a>Tabla usada durante la ejecución:

[\_Tabla de columnas](-columns-table.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 



