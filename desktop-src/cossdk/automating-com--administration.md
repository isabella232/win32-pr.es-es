---
description: COM+ proporciona un modelo de objetos de administración que expone toda la funcionalidad de la herramienta administrativa Servicios de componentes, a su vez un front-end gráfico escrito sobre los objetos administrativos.
ms.assetid: f302eb02-2ef5-42ee-a18f-59f7e60b38df
title: Automatización de la administración de COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0ef3f56da64e442594a7685a77efb9a06e3fe08
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073019"
---
# <a name="automating-com-administration"></a>Automatización de la administración de COM+

COM+ proporciona un modelo de objetos de administración que expone toda la funcionalidad de la herramienta administrativa Servicios de componentes, a su vez un front-end gráfico escrito sobre los objetos administrativos. Puede usar estos objetos, proporcionados por la biblioteca de administración de servicios de componentes (COMAdmin), para automatizar todas las tareas en la administración de aplicaciones y servicios COM+.

Los objetos COMAdmin permiten leer y escribir información almacenada en el catálogo de COM+, el almacén de datos subyacente que contiene todos los datos de configuración de COM+.

Puede usar estos objetos para hacer lo siguiente:

-   Cree y configure aplicaciones COM+.
-   Instale y exporte las aplicaciones COM+ existentes.
-   Administrar aplicaciones COM+ instaladas.
-   Administrar y configurar servicios.
-   Administrar servicios de componentes de forma remota en un equipo diferente.

Puede usar los objetos COMAdmin que pueden incluirse en scripts con cualquier lenguaje compatible con Automation, como Microsoft Visual Basic y Visual Basic Script. Puede desarrollar scripts ligeros o herramientas de administración de uso general. Por ejemplo, puede realizar lo siguiente:

-   Escribir scripts para realizar tareas administrativas rutinarias.
-   Escribir scripts para automatizar procesos en el desarrollo de aplicaciones COM+.
-   Desarrolle herramientas de uso general para administrar y supervisar servicios de componentes.
-   Desarrolle archivos ejecutables de instalación para instalar e implementar la aplicación COM+.

La biblioteca COMAdmin proporciona compatibilidad con versiones anteriores con la biblioteca de administración de MTS 2.0. La mayoría del código de administración de MTS 2.0 existente seguirá funcionando, aunque con algunas excepciones. (Vea [Biblioteca de administración de MTS).](mts-administration-library.md)

Para automatizar la administración de forma eficaz, debe estar familiarizado con las tareas de administración realizadas con la herramienta administrativa Servicios de componentes.

Para obtener descripciones completa de los objetos COMAdmin y las interfaces correspondientes, consulte la documentación de referencia de COM+ para las siguientes clases e interfaces:

-   [**COMAdminCatalog**](comadmincatalog.md)
-   [**COMAdminCatalogCollection**](comadmincatalogcollection.md)
-   [**COMAdminCatalogObject**](comadmincatalogobject.md)
-   [**ICOMAdminCatalog**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog)
-   [**ICOMAdminCatalog2**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog2)
-   [**ICatalogCollection**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogcollection)
-   [**ICatalogObject**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogobject)

En los temas siguientes de esta sección se proporciona información general para automatizar la administración mediante los objetos COMAdmin:

-   [Información general de los objetos COMAdmin](overview-of-the-comadmin-objects.md)
-   [Recuperar colecciones en el catálogo de COM+](retrieving-collections-on-the-com--catalog.md)
-   [Establecimiento de propiedades y guardado de cambios en el catálogo de COM+](setting-properties-and-saving-changes-to-the-com--catalog.md)
-   [Control de errores de administración de COM+](handling-com--administration-errors.md)
-   [Operaciones de administración de COM+ dentro de transacciones](com--administration-operations-within-transactions.md)
-   [Ejemplo introductorio con el catálogo de administración de COM+](introductory-example-using-the-com--administration-catalog.md)

 

 



