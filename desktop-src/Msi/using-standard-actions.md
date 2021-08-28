---
description: Una acción se ejecuta en Windows Installer llamando a la función MsiDoAction o incluyendo la acción en una tabla de secuencia.
ms.assetid: ee5bdc72-adf4-46f4-ae1f-4c41d22a1ed8
title: Uso de acciones estándar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60696e79c12b054739d87ffe5696e898a8eb955c4c7bfe0aa9c2341db7c2d720
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119996215"
---
# <a name="using-standard-actions"></a>Uso de acciones estándar

Una acción se ejecuta en Windows Installer llamando a la función [**MsiDoAction**](/windows/desktop/api/Msiquery/nf-msiquery-msidoactiona) o incluyendo la acción en una tabla de secuencia. Dado que la mayoría de las acciones encapsulan un único propósito, la manera más común de usar acciones es ordenar una serie de acciones en una secuencia para realizar una tarea mayor. El instalador tiene tres acciones estándar de nivel superior que llaman a un conjunto asociado de tablas de secuencia. Estas tablas de secuencia asociadas pueden contener acciones estándar, acciones personalizadas y elementos de interfaz de usuario. Cada acción de una tabla de secuencia tiene un número de secuencia asociado y también puede tener una expresión condicional asociada. Todas las acciones de una tabla de secuencia se visitan en orden y solo se ejecutan si la expresión condicional se evalúa como True.

Aunque una acción estándar puede tener cualquier número de secuencia asociado, muchos tienen restricciones de secuencia que se deben seguir para que la acción funcione correctamente. Por ejemplo, se debe llamar a la acción [FileCost](filecost-action.md)después de [la acción CostInitialize](costinitialize-action.md). Para obtener más información sobre las restricciones de secuenciación de acciones estándar, vea Acciones con [restricciones](actions-with-sequencing-restrictions.md)de secuenciación, Acciones sin [restricciones](actions-without-sequencing-restrictions.md)de secuenciación o Referencia de [acciones estándar.](standard-actions-reference.md)

En los temas siguientes se proporciona más información sobre el uso de acciones estándar.

-   [Publicar productos, características y componentes](publishing-products-features-and-components.md)
-   [Búsqueda de archivos](file-searching.md)
-   [Costo de archivos](file-costing.md)
-   [Instalación de archivos](file-installation.md)
-   [Modificar el Registro](modifying-the-registry.md)
-   [Acciones en ejecución](running-actions.md)

Consulte también Acerca [de acciones estándar o](about-standard-actions.md) Referencia de acciones [estándar.](standard-actions-reference.md)

 

 



