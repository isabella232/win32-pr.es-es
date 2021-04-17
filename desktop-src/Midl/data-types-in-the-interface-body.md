---
title: Tipos de datos en el cuerpo de la interfaz
description: El cuerpo de la interfaz, que se incluye entre llaves (), contiene los tipos de datos que se utilizarán en las llamadas a procedimientos remotos y prototipos para las funciones que se ejecutarán de forma remota.
ms.assetid: a5130744-6b14-48a4-b439-16f0ecaf08c2
keywords:
- interfaces MIDL, tipos de datos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5bdbbb90c4cbecd4a6a4e3cc74ba9775772dd0a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105685498"
---
# <a name="data-types-in-the-interface-body"></a>Tipos de datos en el cuerpo de la interfaz

El cuerpo de la interfaz, que se incluye entre llaves ({}), contiene los tipos de datos que se utilizarán en las llamadas a procedimientos remotos y prototipos para las funciones que se ejecutarán de forma remota. Un cuerpo de la interfaz puede contener importaciones, pragmas, declaraciones de constantes, declaraciones de tipos y declaraciones de función. Excepto en el modo de compatibilidad de OSF, el compilador MIDL también permite declaraciones implícitas en forma de definiciones de variables.

Tenga en cuenta que la especificación de OSF-DCE para las interfaces RPC no permite varias interfaces en un solo archivo IDL. Por lo tanto, si está compilando el modo de compatibilidad de OSF de MIDL ( [**/OSF**](-osf.md)), el archivo IDL solo puede contener una interfaz.

Para obtener información detallada sobre el uso del compilador MIDL para generar bibliotecas de tipos, vea [generar una biblioteca de tipos con MIDL](generating-a-type-library-with-midl-2.md).

En Microsoft RPC, un archivo IDL puede contener varias interfaces y estas interfaces se pueden declarar hacia delante (dentro del archivo IDL que las define). Por ejemplo:

``` syntax
interface ITwo; //forward declaration
interface IOne 
{
...uses ITwo...
}
interface ITwo 
{
...uses IOne...
}
```

 

 




