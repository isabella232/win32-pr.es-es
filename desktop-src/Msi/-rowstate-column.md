---
description: El nombre de la columna reservada \_ RowState representa el estado no persistente asociado a cada fila de la tabla en una tabla de base de datos del instalador.
ms.assetid: ff570b47-7c16-47ae-b1c2-2ecad9266372
title: _RowState columna
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e61a2964d7d11c1c2429ad95e9de2b8bdb148954
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082552"
---
# <a name="_rowstate-column"></a>\_Columna RowState

El nombre de la columna reservada \_ RowState representa el estado no persistente asociado a cada fila de la tabla en una tabla de base de datos del instalador. La pseudocolumna es de tipo [entero](integer.md)y el valor está compuesto de un conjunto de marcadores de bits. Todos los bits son legibles, pero solo se pueden establecer los bits de UserInfo y temporales. Estos datos solo están disponibles siempre que las tablas estén bloqueadas o en uso (es decir, mientras exista una vista que contenga las tablas). En la tabla siguiente se muestran los atributos que puede tener una fila.



| Nombre           | Value | Significado                                                        |
|----------------|-------|----------------------------------------------------------------|
| iraUserInfo    | 0x01  | El atributo es para uso externo. Este valor se puede actualizar.  |
| iraTemporary   | 0x02  | La fila no es persistente. Este valor se puede actualizar.          |
| iraModified    | 0x04  | Se ha actualizado una fila.                                        |
| iraInserted    | 0x08  | Se ha insertado una fila.                                       |
| iraMergeFailed | 0x0F  | Se intentó fusionar mediante combinación con datos no idénticos que no son de clave. |



 

Los bits 6 a 8 están reservados.

 

 



