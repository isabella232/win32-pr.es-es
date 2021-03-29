---
description: COM+ proporciona un modelo de objetos de administración que expone toda la funcionalidad de la herramienta administrativa Servicios de componentes, un front-end gráfico escrito sobre los objetos administrativos.
ms.assetid: f302eb02-2ef5-42ee-a18f-59f7e60b38df
title: Automatizar la administración de COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0ef3f56da64e442594a7685a77efb9a06e3fe08
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153269"
---
# <a name="automating-com-administration"></a>Automatizar la administración de COM+

COM+ proporciona un modelo de objetos de administración que expone toda la funcionalidad de la herramienta administrativa Servicios de componentes, un front-end gráfico escrito sobre los objetos administrativos. Puede usar estos objetos, suministrados por la biblioteca de administración de servicios de componentes (COMAdmin), para automatizar todas las tareas en la administración de aplicaciones y servicios COM+.

Los objetos COMAdmin permiten leer y escribir información que se almacena en el catálogo de COM+, el almacén de datos subyacente que contiene todos los datos de configuración de COM+.

Puede usar estos objetos para hacer lo siguiente:

-   Crear y configurar aplicaciones COM+.
-   Instalar y exportar aplicaciones COM+ existentes.
-   Administrar aplicaciones COM+ instaladas.
-   Administrar y configurar servicios.
-   Administrar servicios de componentes de forma remota en un equipo diferente.

Puede usar los objetos COMAdmin que admiten scripts con cualquier lenguaje compatible con automatización, como Microsoft Visual Basic y Visual Basic Script. Puede desarrollar scripts ligeros o herramientas de administración de uso general. Por ejemplo, puede realizar lo siguiente:

-   Escribir scripts para realizar tareas administrativas rutinarias.
-   Escribir scripts para automatizar procesos en el desarrollo de aplicaciones COM+.
-   Desarrollar herramientas de uso general para administrar y supervisar servicios de componentes.
-   Desarrollar ejecutables de configuración para instalar e implementar la aplicación COM+.

La biblioteca COMAdmin proporciona compatibilidad con versiones anteriores de la biblioteca de administración de MTS 2,0. La mayoría de los códigos existentes de administración de MTS 2,0 seguirán funcionando, aunque con algunas excepciones. (Consulte [biblioteca de administración de MTS](mts-administration-library.md)).

Para automatizar la administración de forma eficaz, debe estar familiarizado con las tareas de administración que se realizan con la herramienta administrativa Servicios de componentes.

Para obtener descripciones completas de los objetos COMAdmin y de las interfaces correspondientes, vea la documentación de referencia de COM+ para las clases e interfaces siguientes:

-   [**COMAdminCatalog**](comadmincatalog.md)
-   [**COMAdminCatalogCollection**](comadmincatalogcollection.md)
-   [**COMAdminCatalogObject**](comadmincatalogobject.md)
-   [**ICOMAdminCatalog**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog)
-   [**ICOMAdminCatalog2**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog2)
-   [**ICatalogCollection**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogcollection)
-   [**ICatalogObject**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogobject)

Los temas siguientes de esta sección proporcionan información general para la automatización de la administración con los objetos COMAdmin:

-   [Información general de los objetos COMAdmin](overview-of-the-comadmin-objects.md)
-   [Recuperar recopilaciones en el catálogo de COM+](retrieving-collections-on-the-com--catalog.md)
-   [Establecer propiedades y guardar cambios en el catálogo de COM+](setting-properties-and-saving-changes-to-the-com--catalog.md)
-   [Control de errores de administración de COM+](handling-com--administration-errors.md)
-   [Operaciones de administración de COM+ en transacciones](com--administration-operations-within-transactions.md)
-   [Ejemplo introductorio con el catálogo de administración de COM+](introductory-example-using-the-com--administration-catalog.md)

 

 



