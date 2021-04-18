---
description: El grupo de tablas de localizador se utiliza para buscar archivos y aplicaciones.
ms.assetid: 44ab770b-1a7f-4590-9681-8f6bd343bf86
title: Grupo de tablas de localizador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 300a869a912c06b2112476f50bcda021833cfbe7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687822"
---
# <a name="locator-tables-group"></a>Grupo de tablas de localizador

El grupo de tablas de localizador se utiliza para buscar archivos y aplicaciones. Para buscar un archivo, primero determine la firma del archivo y, a continuación, busque el archivo. Las tablas de localizador se usan para buscar en el registro, en los datos de configuración del instalador, en el árbol de directorios o en los archivos. ini la firma única de un archivo. A continuación, se puede comprobar la firma de archivo en la [tabla de firma](signature-table.md) para asegurarse de que un archivo determinado es realmente el archivo que se busca y no otro archivo con el mismo nombre. Si un registro de una tabla de localizador no contiene una clave en la tabla de firma, el registro hace referencia a un directorio y no a un archivo.

El componente que controla un archivo se encuentra en la [tabla de archivos](file-table.md) a través de la clave externa de la tabla de [componentes](component-table.md). El instalador resuelve la ubicación de un archivo a través de la tabla de componentes porque cada archivo pertenece a un componente. La ubicación de un componente se encuentra a través de una clave externa en la tabla de componentes en la [tabla de directorios](directory-table.md).

La ubicación de una aplicación se encuentra buscando archivos que componen la aplicación. El instalador también proporciona dos tablas para buscar versiones anteriores de una aplicación: la [tabla AppSearch](appsearch-table.md) y la [tabla CCPSearch](ccpsearch-table.md).

En las tablas siguientes se compone el grupo de tablas de localizador y se usan para determinar la firma del archivo.

-   La [tabla RegLocator](reglocator-table.md) contiene la información necesaria para buscar un archivo o un directorio en el registro.
-   La [tabla IniLocator](inilocator-table.md) contiene la información necesaria para buscar un archivo. ini. El archivo. ini debe estar presente en el directorio predeterminado de Microsoft Windows.
-   La [tabla CompLocator](complocator-table.md) contiene la información necesaria para buscar un archivo o un directorio con los datos de configuración del instalador.
-   La [tabla DrLocator](drlocator-table.md) contiene la información necesaria para buscar un archivo o un directorio en el árbol de directorios.
-   La [tabla AppSearch](appsearch-table.md) contiene las propiedades que se deben establecer en el resultado de la búsqueda de una firma de archivo correspondiente.
-   La [tabla CCPSearch](ccpsearch-table.md) contiene la lista de firmas de archivo, al menos una de las cuales debe estar presente en el equipo de un usuario para el programa de comprobación de cumplimiento (CCP).

 

 



