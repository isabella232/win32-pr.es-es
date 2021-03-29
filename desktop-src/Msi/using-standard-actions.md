---
description: Una acción se ejecuta en el Windows Installer llamando a la función MsiDoAction o incluyendo la acción en una tabla de secuencia.
ms.assetid: ee5bdc72-adf4-46f4-ae1f-4c41d22a1ed8
title: Uso de acciones estándar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f52118580f4e18f07f86bd15da73f9aafb453c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652547"
---
# <a name="using-standard-actions"></a>Uso de acciones estándar

Una acción se ejecuta en el Windows Installer llamando a la función [**MsiDoAction**](/windows/desktop/api/Msiquery/nf-msiquery-msidoactiona) o incluyendo la acción en una tabla de secuencia. Dado que la mayoría de las acciones encapsulan un solo propósito, la manera más común de usar acciones es ordenar una serie de acciones en una secuencia para realizar una tarea más grande. El instalador tiene tres acciones de nivel superior estándar que llaman a un conjunto asociado de tablas de secuencia. Estas tablas de secuencia asociadas pueden contener acciones estándar, acciones personalizadas y elementos de la interfaz de usuario. Cada acción de una tabla de secuencia tiene un número de secuencia asociado y también puede tener una expresión condicional asociada. Todas las acciones de una tabla de secuencia se visitan en orden y solo se ejecutan si la expresión condicional se evalúa como true.

Aunque una acción estándar puede tener cualquier número de secuencia asociado, muchas tienen restricciones de secuencia que deben seguirse para que la acción funcione correctamente. Por ejemplo, la [acción FileCost](filecost-action.md)debe llamarse después de la [acción CostInitialize](costinitialize-action.md). Para obtener más información sobre las restricciones de la secuencia de acciones estándar, vea [acciones con restricciones de secuenciación](actions-with-sequencing-restrictions.md), [acciones sin restricciones de secuenciación](actions-without-sequencing-restrictions.md)o [referencia de acciones estándar](standard-actions-reference.md).

En los temas siguientes se proporciona más información acerca del uso de las acciones estándar.

-   [Publicar productos, características y componentes](publishing-products-features-and-components.md)
-   [Búsqueda de archivos](file-searching.md)
-   [Costo de archivos](file-costing.md)
-   [Instalación de archivos](file-installation.md)
-   [Modificar el registro](modifying-the-registry.md)
-   [Ejecutar acciones](running-actions.md)

Vea también [sobre acciones estándar](about-standard-actions.md) o [referencia de acciones estándar](standard-actions-reference.md).

 

 



