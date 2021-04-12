---
description: Antes de trabajar con una base de datos, primero debe obtener un identificador.
ms.assetid: 53cf73bc-4d52-471c-8384-46d106a36e38
title: Obtener un identificador de base de datos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec5f37f1abd329d0c51b00839d43ef85784fdad1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155285"
---
# <a name="obtaining-a-database-handle"></a>Obtener un identificador de base de datos

Antes de trabajar con una base de datos, primero debe obtener un identificador.

**Para obtener acceso a información sobre una base de datos del instalador**

1.  Obtenga un identificador de la base de datos de una de las dos maneras siguientes:
    -   Si hay una instalación en curso, obtenga un identificador de la base de datos activa mediante una llamada a la función [**MsiGetActiveDatabase**](/windows/desktop/api/Msiquery/nf-msiquery-msigetactivedatabase) .
    -   Si una instalación no está en curso, abra cualquier base de datos especificada llamando a la función [**MsiOpenDatabase**](/windows/desktop/api/Msiquery/nf-msiquery-msiopendatabasea) .
2.  Una vez abierta la base de datos, puede llamar a funciones para obtener información sobre la base de datos o para manipular la base de datos.
    -   Cree un objeto de **vista** y especifique una consulta SQL de la base de datos abierta mediante una llamada a la función [**MsiDatabaseOpenView**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseopenviewa) .
    -   Obtener un registro que contenga todas las claves principales de una tabla especificada en la base de datos abierta mediante una llamada a la función [**MsiDatabaseGetPrimaryKeys**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegetprimarykeysa) .
    -   Compruebe el estado actual de una base de datos abierta mediante una llamada a la función [**MsiGetDatabaseState**](/windows/desktop/api/Msiquery/nf-msiquery-msigetdatabasestate) . Con la función **MsiGetDatabaseState** , puede determinar el estado de lectura y escritura de una base de datos o si el identificador es válido.

 

 



