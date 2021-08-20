---
description: Los cambios realizados en la base de datos de instalación no se escriben en la base de datos hasta que se llama a MsiDatabaseCommit.
ms.assetid: 65271631-457c-4d3e-9384-126d2c9d63d7
title: Confirmar bases de datos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1ab5f4da5b82fb3b6b2ac7d2371bd8046ab87a23d2ef43b6473f7e36a4771a2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118145354"
---
# <a name="committing-databases"></a>Confirmar bases de datos

Los cambios realizados en la base de datos de instalación no se escriben en la base de datos hasta que se llama a [**MsiDatabaseCommit.**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit)

**Para asegurarse de que los cambios realizados en una base de datos se han finalizado**

1.  Compruebe si se escribirá una tabla al llamar a [**MsiDatabaseCommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit) mediante una llamada a [**MsiDatabaseIsTablePersistent.**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseistablepersistenta)
2.  Llame a la [**función MsiDatabaseCommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit) para finalizar los cambios en la base de datos.

Los cambios realizados en una base de datos se acumulan y no se reflejan en la base de datos real hasta que se llama a [**MsiDatabaseCommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit). Las columnas o filas temporales no se confirman en la base de datos. Cuando se cierra una base de datos, todos los cambios realizados desde el **último MsiDatabaseCommit** se revierte automáticamente.

 

 



