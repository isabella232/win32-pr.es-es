---
description: Los cambios realizados en la base de datos de instalación no se escriben en la base de datos hasta que se llama a MsiDatabaseCommit.
ms.assetid: 65271631-457c-4d3e-9384-126d2c9d63d7
title: Confirmar bases de datos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1336b094703e61b14966e7a73a6e67f73762024
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911342"
---
# <a name="committing-databases"></a>Confirmar bases de datos

Los cambios realizados en la base de datos de instalación no se escriben en la base de datos hasta que se llama a [**MsiDatabaseCommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit).

**Para asegurarse de que se finalizan los cambios realizados en una base de datos**

1.  Compruebe si una tabla se escribirá al llamar a [**MsiDatabaseCommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit) llamando a [**MsiDatabaseIsTablePersistent**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseistablepersistenta).
2.  Llame a la función [**MsiDatabaseCommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit) para finalizar los cambios en la base de datos.

Los cambios realizados en una base de datos se acumulan y no se reflejan en la base de datos real hasta que se llama a [**MsiDatabaseCommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit). Las columnas o filas temporales no se confirman en la base de datos. Cuando se cierra una base de datos, se revierten automáticamente todos los cambios realizados desde el último **MsiDatabaseCommit** .

 

 



