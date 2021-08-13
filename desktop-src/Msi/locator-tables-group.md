---
description: El grupo Tablas de localizadores se usa para buscar archivos y aplicaciones.
ms.assetid: 44ab770b-1a7f-4590-9681-8f6bd343bf86
title: Grupo de tablas de localizador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ad0cf5b2d28d01b6e10cf796dc9653c82feb8ffb63adc57c7a7bc244e7ccfcb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118629172"
---
# <a name="locator-tables-group"></a>Grupo de tablas de localizador

El grupo Tablas de localizadores se usa para buscar archivos y aplicaciones. Para buscar un archivo, primero determine la firma del archivo y, a continuación, busque el archivo. Las tablas Locator se usan para buscar en el Registro, los datos de configuración del instalador, el árbol de directorios o .ini archivos para la firma única de un archivo. La firma de archivo se puede comprobar en la tabla [Firma](signature-table.md) para determinar que un archivo determinado es realmente el archivo que se está buscando y no otro archivo con el mismo nombre. Si un registro de una tabla de localizador no contiene una clave en la tabla Signature, el registro hace referencia a un directorio y no a un archivo.

El componente que controla un archivo se encuentra en la [tabla File a](file-table.md) través de la clave externa de la tabla [Component](component-table.md). El instalador resuelve la ubicación de un archivo a través de la tabla Component porque cada archivo pertenece a un componente. La ubicación de un componente se encuentra a través de una clave externa en la tabla Component de la [tabla Directory](directory-table.md).

Para encontrar la ubicación de una aplicación, busque los archivos que la conste. El instalador también proporciona dos tablas para buscar versiones anteriores de una aplicación: la [tabla AppSearch](appsearch-table.md) y [la tabla CCPSearch](ccpsearch-table.md).

Las tablas siguientes son el grupo Tablas de localizador y se usan para determinar la firma del archivo.

-   La [tabla RegLocator](reglocator-table.md) contiene la información necesaria para buscar un archivo o directorio en el Registro.
-   La [tabla IniLocator](inilocator-table.md) contiene la información necesaria para buscar un .ini archivo. El .ini debe estar presente en el directorio predeterminado de Microsoft Windows.
-   La [tabla CompLocator](complocator-table.md) contiene la información necesaria para buscar un archivo o un directorio mediante los datos de configuración del instalador.
-   La [tabla DrLocator](drlocator-table.md) contiene la información necesaria para buscar un archivo o directorio en el árbol de directorios.
-   La [tabla AppSearch contiene](appsearch-table.md) las propiedades que se deben establecer en el resultado de la búsqueda de una firma de archivo correspondiente.
-   La [tabla CCPSearch](ccpsearch-table.md) contiene la lista de firmas de archivo, al menos una de las cuales debe estar presente en el equipo de un usuario para el Programa de comprobación de cumplimiento (CCP).

 

 



