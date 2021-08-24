---
description: Los desarrolladores de bases de datos de instalación deben tener en cuenta dos limitaciones en el control de flujos mediante la implementación de almacenamiento estructurado OLE de Win32.
ms.assetid: ebd5fcac-0238-4f30-9fd5-a0c5cf9028ef
title: Limitaciones de OLE Secuencias
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69a3a1c606a4446129d9e6592c9b352dd0b3e06ae5c77bb378c2430a32cbc568
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119754255"
---
# <a name="ole-limitations-on-streams"></a>Limitaciones de OLE Secuencias

Los desarrolladores de bases de datos de instalación deben tener en cuenta dos limitaciones en el control de flujos mediante la implementación de almacenamiento estructurado OLE de Win32. Estas limitaciones pueden afectar indirectamente a las funciones del instalador a través de transformaciones y otros datos que se pueden almacenar en la base de datos como una secuencia.

Hay dos limitaciones pertinentes:

-   Los datos binarios se almacenan con un nombre de índice creado mediante la concatenación del nombre de tabla y los valores de las claves principales del registro mediante un delimitador de punto. OLE limita los nombres de secuencia a 32 caracteres (31 + terminador nulo). Windows El instalador usa un algoritmo de compresión que puede expandir el límite a 62 caracteres en función del carácter. Tenga en cuenta que los caracteres de doble byte cuentan como 2.
-   Aunque puede tener varias secuencias abiertas a la vez, no puede abrir una secuencia una segunda vez hasta que se cierre la primera referencia. Esto significa que no puede seleccionar el mismo flujo de datos binario para que se abra en varios registros simultáneamente. Se producirá un error al intentar leer los datos binarios del segundo registro. Tampoco puede cambiar el nombre de las claves principales de un registro mientras esté abierto un flujo de datos binario en ese registro.

 

 



