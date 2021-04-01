---
description: Los desarrolladores de bases de datos de instalación deben tener en cuenta dos limitaciones en el control de secuencias mediante la implementación de almacenamiento estructurado OLE de Win32.
ms.assetid: ebd5fcac-0238-4f30-9fd5-a0c5cf9028ef
title: Limitaciones de OLE en secuencias
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8ccf2a259b004605381792a4eb9da62d329be91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275758"
---
# <a name="ole-limitations-on-streams"></a>Limitaciones de OLE en secuencias

Los desarrolladores de bases de datos de instalación deben tener en cuenta dos limitaciones en el control de secuencias mediante la implementación de almacenamiento estructurado OLE de Win32. Estas limitaciones pueden afectar a las funciones de instalador de manera indirecta a través de transformaciones y otros datos que se pueden almacenar en la base de datos como una secuencia.

Hay dos limitaciones relevantes:

-   Los datos binarios se almacenan con un nombre de índice creado mediante la concatenación del nombre de tabla y los valores de las claves principales del registro mediante un delimitador de punto. OLE limita los nombres de secuencia a 32 caracteres (31 + terminador nulo). Windows Installer usa un algoritmo de compresión que puede expandir el límite hasta 62 caracteres en función del carácter. Tenga en cuenta que el número de caracteres de doble byte es 2.
-   Aunque puede tener varias secuencias abiertas al mismo tiempo, no puede abrir un flujo por segunda vez hasta que se cierre la primera referencia. Esto significa que no se puede seleccionar el mismo flujo de datos binarios que se va a abrir en varios registros simultáneamente. Se produce un error al intentar leer los datos binarios del segundo registro. Tampoco puede cambiar el nombre de las claves principales de un registro mientras haya un flujo de datos binarios en ese registro abierto.

 

 



