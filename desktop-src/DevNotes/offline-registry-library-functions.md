---
description: A continuación se enumeran las funciones de la biblioteca del registro sin conexión.
ms.assetid: 378811d2-064c-4d81-979e-392097d55baa
title: Funciones de la biblioteca del registro sin conexión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0c36afac0b8f5f0aed17b12a7e0562cce75ea69
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423247"
---
# <a name="offline-registry-library-functions"></a>Funciones de la biblioteca del registro sin conexión

A continuación se enumeran las funciones de la biblioteca del registro sin conexión.



| Función                                       | Descripción                                                                                                         |
|------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [**ORCloseHive**](orclosehive.md)             | Cierra el subárbol del registro sin conexión especificado y libera la memoria asignada para el subárbol.                                 |
| [**ORCloseKey**](orclosekey.md)               | Cierra un identificador de la clave del registro especificada en un subárbol del registro sin conexión.                                          |
| [**ORCreateHive**](orcreatehive.md)           | Crea un subárbol del registro sin conexión que contiene una única clave raíz vacía.                                             |
| [**ORCreateKey**](orcreatekey.md)             | Crea la clave del registro especificada en un subárbol del registro sin conexión. Si la clave ya existe, la función la abre.   |
| [**ORDeleteKey**](ordeletekey.md)             | Elimina una subclave y sus valores de un subárbol del registro sin conexión.                                                      |
| [**ORDeleteValue**](ordeletevalue.md)         | Quita un valor de la clave del registro especificada en un subárbol del registro sin conexión.                                        |
| [**OREnumKey**](orenumkey.md)                 | Enumera las subclaves de la clave del registro abierta especificada en un subárbol del registro sin conexión.                              |
| [**OREnumValue**](orenumvalue.md)             | Enumera los valores de la clave del registro abierta especificada en un subárbol del registro sin conexión.                              |
| [**ORGetKeySecurity**](orgetkeysecurity.md)   | Recupera una copia del descriptor de seguridad que protege la clave del registro abierta especificada en un subárbol del registro sin conexión. |
| [**ORGetValue**](orgetvalue.md)               | Recupera el tipo y los datos para el valor del registro especificado en un subárbol del registro sin conexión.                           |
| [**ORGetVersion**](orgetversion.md)           | Recupera la versión de la biblioteca del registro sin conexión.                                                              |
| [**ORGetVirtualFlags**](orgetvirtualflags.md) | Recupera las marcas virtuales de la clave del registro abierta especificada en un subárbol del registro sin conexión.                         |
| [**OROpenHive**](oropenhive.md)               | Carga el archivo de Hive especificado en la memoria y valida el subárbol.                                                   |
| [**OROpenKey**](oropenkey.md)                 | Abre la clave del registro especificada en un subárbol del registro sin conexión.                                                       |
| [**ORQueryInfoKey**](orqueryinfokey.md)       | Recupera información acerca de la clave del registro especificada en un subárbol del registro sin conexión.                                 |
| [**ORSaveHive**](orsavehive.md)               | Escribe el subárbol del registro sin conexión especificado en un archivo.                                                               |
| [**ORSetKeySecurity**](orsetkeysecurity.md)   | Establece la seguridad de una clave del registro abierta en un subárbol del registro sin conexión.                                              |
| [**ORSetValue**](orsetvalue.md)               | Establece los datos para el valor de una clave del registro especificada en un subárbol del registro sin conexión.                                |
| [**ORSetVirtualFlags**](orsetvirtualflags.md) | Establece las marcas de virtualización en la clave del registro abierta especificada en un subárbol del registro sin conexión.                           |



 

 

 



