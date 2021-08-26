---
description: Las claves del Registro se pueden escribir en el registro del sistema una vez instalados todos los componentes seleccionados y sus archivos relacionados.
ms.assetid: b3b39471-85b1-4361-94fd-19d0f0ee2b78
title: Modificar el Registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06f1bd6145811097fcaf74f0622ac35412891d6aa0007c4411099ade6afddd36
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082865"
---
# <a name="modifying-the-registry"></a>Modificar el Registro

Las claves del Registro se pueden escribir en el registro del sistema una vez instalados todos los componentes seleccionados y sus archivos relacionados. Las acciones estándar relacionadas con la modificación del Registro deben secuenciarse después de las acciones estándar de instalación de archivos porque las claves del Registro no se pueden escribir a menos que el componente y el archivo correspondientes se hayan instalado correctamente.

La [acción RegisterClassInfo tiene](registerclassinfo-action.md) acceso a la tabla [Class](class-table.md) para registrar la información de clase COM de los componentes instalados.

La [acción RegisterExtensionInfo](registerextensioninfo-action.md) consulta la tabla [Extension](extension-table.md) y la tabla [Verb](verb-table.md) y registra las extensiones y la información de verbo de comando correspondientes con el sistema operativo.

La [acción RegisterProgIdInfo](registerprogidinfo-action.md) administra el registro de información de OLE ProgId con el sistema operativo.

La [acción RegisterMIMEInfo](registermimeinfo-action.md) procesa la tabla [MIME](mime-table.md) para registrar la asociación entre un tipo de contexto MIME, la extensión de nombre de archivo y el CLSID.

La [acción WriteRegistryValues](writeregistryvalues-action.md) procesa la tabla [del](registry-table.md) Registro y escribe las claves de todos los componentes que se han instalado localmente o que se ejecutan desde el origen. La tabla del Registro permite escribir claves en los subárboles del Registro **HKEY \_ CLASSES \_ ROOT**, **HKEY \_ CURRENT \_ USER**, **HKEY LOCAL \_ \_ MACHINE** y **HKEY \_ USERS.**

La [acción RemoveRegistryValues](removeregistryvalues-action.md) quita las claves que se han marcado para eliminarse en la columna Name de la tabla [Registry](registry-table.md) o [removeRegistry Table](removeregistry-table.md).

La [acción RegisterTypeLibraries](registertypelibraries-action.md) procesa la [tabla TypeLib](typelib-table.md) y registra las bibliotecas de tipos instaladas en el sistema.

 

 



