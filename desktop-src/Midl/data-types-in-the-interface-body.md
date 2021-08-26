---
title: Tipos de datos en el cuerpo de la interfaz
description: El cuerpo de la interfaz, que se incluye entre llaves ( ), contiene los tipos de datos que se usarán en llamadas a procedimientos remotos y prototipos para las funciones que se ejecutarán de forma remota.
ms.assetid: a5130744-6b14-48a4-b439-16f0ecaf08c2
keywords:
- interfaces MIDL, tipos de datos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6691ccf89e1bff3b0e980678a30c6f706b724e4f30192d7960183c00cc00c237
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119979715"
---
# <a name="data-types-in-the-interface-body"></a>Tipos de datos en el cuerpo de la interfaz

El cuerpo de la interfaz, que se incluye entre llaves ({ }), contiene los tipos de datos que se usarán en llamadas a procedimientos remotos y prototipos para las funciones que se ejecutarán de forma remota. Un cuerpo de interfaz puede contener importaciones, pragmas, declaraciones constantes, declaraciones de tipo y declaraciones de función. Excepto en el modo de compatibilidad con OSF, el compilador MIDL también permite declaraciones implícitas en forma de definiciones de variables.

Tenga en cuenta que la especificación OSF-DCE para las interfaces RPC no permite varias interfaces en un único archivo IDL. Por lo tanto, si va a compilar en el modo de compatibilidad con OSF de MIDL ( [**/osf),**](-osf.md)el archivo IDL solo puede contener una interfaz.

Para obtener más información sobre el uso del compilador MIDL para generar bibliotecas de tipos, vea Generar una [biblioteca de tipos con MIDL.](generating-a-type-library-with-midl-2.md)

En RPC de Microsoft, un archivo IDL puede contener varias interfaces y estas interfaces se pueden declarar como reenviadas (dentro del archivo IDL que las define). Por ejemplo:

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

 

 




