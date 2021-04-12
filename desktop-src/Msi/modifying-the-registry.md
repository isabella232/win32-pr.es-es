---
description: Las claves del registro se pueden escribir en el registro del sistema una vez instalados todos los componentes seleccionados y sus archivos relacionados.
ms.assetid: b3b39471-85b1-4361-94fd-19d0f0ee2b78
title: Modificar el registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff6ff79ce340b0487c179cb37e44dff9f42e4be8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361304"
---
# <a name="modifying-the-registry"></a>Modificar el registro

Las claves del registro se pueden escribir en el registro del sistema una vez instalados todos los componentes seleccionados y sus archivos relacionados. Las acciones estándar relacionadas con la modificación del registro se deben secuenciar después de las acciones estándar de instalación de archivos, ya que las claves del registro no se pueden escribir a menos que el componente y el archivo correspondientes se hayan instalado correctamente.

La [acción RegisterClassInfo](registerclassinfo-action.md) tiene acceso a la [tabla de clases](class-table.md) para registrar la información de clase com de los componentes instalados.

La [acción RegisterExtensionInfo](registerextensioninfo-action.md) consulta la tabla de [extensión](extension-table.md) y la [tabla de verbos](verb-table.md) y registra las extensiones y la información de verbo de comando correspondientes en el sistema operativo.

La [acción RegisterProgIdInfo](registerprogidinfo-action.md) administra el registro de información de ID. de ensamblado OLE con el sistema operativo.

La [acción RegisterMIMEInfo](registermimeinfo-action.md) procesa la [tabla MIME](mime-table.md) para registrar la asociación entre un tipo de contexto MIME, la extensión de nombre de archivo y el CLSID.

La [acción WriteRegistryValues](writeregistryvalues-action.md) procesa la [tabla del registro](registry-table.md) y escribe las claves de todos los componentes que se han instalado localmente o que se ejecutan desde el origen. La tabla del registro permite escribir claves en los subárboles del registro de **\_ las clases HKEY \_ root**, **HKEY \_ Current \_ User**, **HKEY \_ local \_ Machine** y **HKEY \_ users** .

La [acción RemoveRegistryValues](removeregistryvalues-action.md) quita las claves que se han marcado para su eliminación en la columna Nombre de la [tabla del registro](registry-table.md) o la [tabla RemoveRegistry](removeregistry-table.md).

La [acción RegisterTypeLibraries](registertypelibraries-action.md) procesa la [tabla typelib](typelib-table.md) y registra las bibliotecas de tipos instaladas con el sistema.

 

 



