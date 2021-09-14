---
title: Generación de UUID de interfaz
description: Generación de identificadores únicos universales (UUID) de interfaz y uso de Uuidgen.
ms.assetid: a973b7f9-71c5-46a0-aa0c-51f150560dbc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68c5f727ed3e37139d4da50f84c3929bff333156
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127244719"
---
# <a name="generating-interface-uuids"></a>Generación de UUID de interfaz

En esta sección se presenta información sobre los identificadores únicos universales (UUID) y la utilidad Uuidgen en los temas siguientes:

-   [¿Qué es un UUID?](#what-is-a-uuid)
-   [Uso de Uuidgen](#using-uuidgen)

## <a name="what-is-a-uuid"></a>¿Qué es un UUID?

Todas las interfaces deben identificarse de forma única en una red para que los clientes puedan encontrarlas. En redes pequeñas, el nombre de la interfaz por sí solo puede ser suficiente para identificarla. Sin embargo, esto no suele ser factible en redes grandes. Por lo tanto, los desarrolladores suelen asignar un identificador único universal (UUID, intercambiable con el término GUID o identificador único global) a cada interfaz. Un UUID es una cadena que contiene un conjunto de dígitos hexadecimales. Cada interfaz tiene un UUID diferente. Para obtener más información, vea [String UUID](string-uuid.md).

La representación textual de un UUID es una cadena que consta de 8 dígitos hexadecimales seguidos de un guion, seguido de tres grupos separados por guiones de 4 dígitos hexadecimales, seguidos de un guion, seguido de 12 dígitos hexadecimales. El ejemplo siguiente es una cadena UUID válida:

ba209999-0c6c-11d2-97cf-00c04f8eea45

Los UUID vacíos se conocen como UUID  nulos en lugar de UUID NULL. El término nulo indica cualquier cosa que sea cero, en blanco, vacía o sin inicializar. Una cadena vacía, un registro de base de datos vacío o un UUID sin inicializar son ejemplos de valores nulos.

> [!Note]  
> El valor **NULL** es el valor específico cero. A menudo se usa en la programación de C y C++ junto con punteros. Nil es un término más general que **NULL.** Los UUID de la interfaz de objeto sin inicializar siempre deben  denominarse UUID nulos en lugar de UUID NULL.

 

## <a name="using-uuidgen"></a>Uso de Uuidgen

Microsoft proporciona un programa de utilidad denominado Uuidgen para generar los UUID. La utilidad Uuidgen genera el UUID en formato de archivo IDL o en formato de lenguaje C.

Al ejecutar la utilidad Uuidgen desde la línea de comandos, puede usar los siguientes modificadores de comandos.



| Modificador uuidgen           | Descripción                                                                |
|--------------------------|----------------------------------------------------------------------------|
| **/I**                   | Genera UUID en una plantilla de interfaz IDL.                                 |
| **/s**                   | Genera UUID como una estructura de C inicializada.                                |
| **/o** < *filename*> | Redirige la salida a un archivo; se especifica inmediatamente después del **modificador /o.** |
| **/n** < *number*>   | Especifica el número de UUID que se generarán.                                 |
| **/v**                   | Muestra información de versión sobre Uuidgen.                                |
| **/h** o **?**          | Muestra el resumen de la opción de comando.                                           |



 

Normalmente, usará la utilidad Uuidgen como se muestra en el ejemplo siguiente.

**uuidgen -i -oMyApp.idl**

Este comando genera un UUID y lo almacena en un archivo MIDL que puede usar como plantilla. Cuando se ejecuta el comando anterior, el contenido de MyApp.idl es similar al siguiente:

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

 

 




