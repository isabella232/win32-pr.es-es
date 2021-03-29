---
title: Generando interfaz UUID
description: Generando identificadores únicos universales (UUID) de interfaz y usando Uuidgen.
ms.assetid: a973b7f9-71c5-46a0-aa0c-51f150560dbc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68c5f727ed3e37139d4da50f84c3929bff333156
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103775739"
---
# <a name="generating-interface-uuids"></a>Generando interfaz UUID

En esta sección se ofrece información sobre los identificadores únicos universales (UUID) y la utilidad uuidgen en los temas siguientes:

-   [¿Qué es un UUID?](#what-is-a-uuid)
-   [Usar uuidgen](#using-uuidgen)

## <a name="what-is-a-uuid"></a>¿Qué es un UUID?

Todas las interfaces se deben identificar de forma única en una red para que los clientes puedan encontrarlas. En redes pequeñas, el nombre de la interfaz solo puede ser suficiente para identificarla. Sin embargo, esto no suele ser factible en redes de gran tamaño. Por lo tanto, los desarrolladores suelen asignar un identificador único universal (UUID, intercambiable con el término GUID o un identificador único global) a cada interfaz. Un UUID es una cadena que contiene un conjunto de dígitos hexadecimales. Cada interfaz tiene un UUID diferente. Para obtener más información, consulte [UUID de cadena](string-uuid.md).

La representación textual de un UUID es una cadena que consta de 8 dígitos hexadecimales seguidos de un guión, seguido de tres grupos separados por guiones de 4 dígitos hexadecimales, seguidos de un guión, seguido de 12 dígitos hexadecimales. El ejemplo siguiente es una cadena de UUID válida:

ba209999-0c6c-11d2-97cf-00c04f8eea45

Los UUID vacíos se denominan un UUID nulo en lugar de un UUID **nulo** . El término Nil indica cualquier elemento que sea cero, en blanco, vacío o no inicializado. Una cadena vacía, un registro de base de datos vacío o un UUID no inicializado son ejemplos de valores nulos.

> [!Note]  
> El valor **null** es el valor específico de cero. A menudo se usa en la programación de C y C++ junto con punteros. Nil es un término más general que **null**. La interfaz de objeto no inicializada UUID siempre se debe denominar UUID nulo en lugar de UUID **nulo** .

 

## <a name="using-uuidgen"></a>Usar uuidgen

Microsoft proporciona un programa de utilidad denominado uuidgen para generar el UUID. La utilidad uuidgen genera el UUID en formato de archivo IDL o en formato de lenguaje C.

Al ejecutar la utilidad uuidgen desde la línea de comandos, puede usar los siguientes modificadores de comando.



| Uuidgen (conmutador)           | Descripción                                                                |
|--------------------------|----------------------------------------------------------------------------|
| **/I**                   | Genera UUID en una plantilla de interfaz IDL.                                 |
| **/s**                   | Genera UUID como una estructura de C inicializada.                                |
| **/o** < *nombre de archivo*> | Redirige la salida a un archivo; se especifica inmediatamente después del modificador **/o** . |
| **/n** < *número* de>   | Especifica el número de UUID que se va a generar.                                 |
| **/v**                   | Muestra información de versión sobre Uuidgen.                                |
| **/h** o **?**          | Muestra el Resumen de la opción de comando.                                           |



 

Normalmente, utilizará la utilidad uuidgen, tal como se muestra en el ejemplo siguiente.

**uuidgen-i-oMyApp. idl**

Este comando genera un UUID y lo almacena en un archivo MIDL que se puede utilizar como plantilla. Cuando se ejecuta el comando anterior, el contenido de MyApp. idl es similar al siguiente:

``` syntax
[
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45),
  version(1.0)
]
interface INTERFACENAME
{

}
```

El siguiente paso sería reemplazar el nombre del marcador de posición, INTERFACENAME, por el nombre real de la interfaz.

 

 




