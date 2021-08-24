---
description: El nombre de columna reservada RowState representa el estado no persistente asociado a \_ cada fila de tabla de una tabla de base de datos del instalador.
ms.assetid: ff570b47-7c16-47ae-b1c2-2ecad9266372
title: _RowState columna
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42e0164b76589dfa76deb8754df3e11a8b8250a43d791dec92d0fee65dfb719b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119146098"
---
# <a name="_rowstate-column"></a>\_Columna RowState

El nombre de columna reservada RowState representa el estado no persistente asociado a \_ cada fila de tabla de una tabla de base de datos del instalador. La pseudo column es de tipo [Integer](integer.md)y el valor consta de un conjunto de marcas de bits. Todos los bits son legibles, pero solo se pueden establecer los bits UserInfo y Temporary. Estos datos solo están disponibles siempre que las tablas estén bloqueadas o en uso (es decir, mientras exista una vista que contenga las tablas). En la tabla siguiente se muestran los atributos que puede tener una fila.



| Nombre           | Value | Significado                                                        |
|----------------|-------|----------------------------------------------------------------|
| infousuario    | 0x01  | El atributo es para uso externo. Este valor se puede actualizar.  |
| resalte   | 0x02  | La fila no es persistente. Este valor se puede actualizar.          |
| lugarModified    | 0x04  | Se ha actualizado una fila.                                        |
| reserted    | 0x08  | Se ha insertado una fila.                                       |
| mergeMergeFailed | 0x0F  | Se intentó combinar con datos no idénticos y no clave. |



 

Los bits del 6 al 8 están reservados.

 

 



