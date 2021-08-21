---
description: La biblioteca del Registro sin conexión se usa para modificar un subárbol del Registro fuera del registro del sistema activo.
ms.assetid: 61db2804-1b67-473f-8dd7-6be6c6a7184e
title: Acerca de la biblioteca del Registro sin conexión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5c2aecf71e8e42ad96c018bb613d7aac9a4a867bb301671e9553f1768a4ce44
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118956189"
---
# <a name="about-the-offline-registry-library"></a>Acerca de la biblioteca del Registro sin conexión

La biblioteca del Registro sin conexión se usa para modificar un subárbol del Registro fuera del registro del sistema activo.

La biblioteca del Registro sin conexión está pensada para escenarios de actualización del Registro, como el mantenimiento de una imagen de sistema operativo. Las funciones del Registro sin conexión proporcionan las siguientes funcionalidades que no están disponibles con las funciones del Registro estándar:

-   Las funciones del Registro sin conexión se pueden usar para modificar un subárbol del Registro en cualquier formato de registro compatible. Las funciones del Registro estándar solo pueden realizar cambios en un subárbol del Registro activo y los cambios deben ser compatibles con la versión de Windows que se ejecuta en el sistema.
-   La biblioteca del Registro sin conexión solo requiere acceso de lectura para abrir un archivo de Hive del Registro y acceso de escritura para guardar el archivo. No se realizan otras comprobaciones de acceso en objetos del subárbol, lo que permite modificar el subárbol con privilegios de usuario estándar. Con las funciones del Registro estándar, cargar un subárbol en el registro activo es una operación con privilegios que requiere acceso administrativo.

Las funciones del Registro sin conexión no deben usarse como sustituto de las funciones del Registro del sistema por los siguientes motivos:

-   Es imposible compartir subárboles del Registro entre procesos mediante las funciones del Registro sin conexión.
-   Las funciones del Registro sin conexión usan un bloqueo simple que puede provocar una degradación grave del rendimiento de las aplicaciones multiproceso.
-   Los cambios realizados con las funciones del Registro sin conexión no se guardan hasta que se llama a la función [**ORSaveHive.**](orsavehive.md)

Las aplicaciones no deben usar las funciones del registro sin conexión para omitir los requisitos de seguridad del registro del sistema. Para cargar un subárbol, una aplicación que se ejecuta sin los privilegios especiales requeridos por la [función RegLoadKey](/windows/win32/api/winreg/nf-winreg-regloadkeya) puede usar la [función RegLoadAppKey.](/windows/win32/api/winreg/nf-winreg-regloadappkeya)

**Windows Server 2003 y Windows XP:** No [se admite la función RegLoadAppKey.](/windows/win32/api/winreg/nf-winreg-regloadappkeya)

Un *subárbol del Registro* sin conexión es un subárbol del Registro que se ha cargado en la memoria mediante las funciones del Registro sin conexión. Para crear un subárbol del Registro sin conexión vacío, use la [**función ORCreateHive.**](orcreatehive.md) Para modificar un subárbol del Registro existente, use las funciones [RegSaveKey](/windows/win32/api/winreg/nf-winreg-regsavekeya) o [RegSaveKeyEx](/windows/win32/api/winreg/nf-winreg-regsavekeyexa) para guardar un subárbol del registro del sistema activo en un archivo y, a continuación, use la función [**OROpenHive**](oropenhive.md) para abrir el archivo.

Las [**funciones ORCreateHive**](orcreatehive.md) [**y OROpenHive**](oropenhive.md) devuelven un identificador a la clave raíz del subárbol del Registro sin conexión. Este identificador se puede usar como un identificador para cualquier otra clave del subárbol del Registro sin conexión con las siguientes excepciones: las funciones [**ORCreateKey**](orcreatekey.md) y [**OROpenKey**](oropenkey.md) no se pueden usar para devolver un identificador a la clave raíz; La [**función ORCloseKey**](orclosekey.md) no se puede usar para cerrar la clave raíz; y la [**función ORDeleteKey**](ordeletekey.md) no se puede usar para eliminar la clave raíz. En todos estos casos, se produce un error en la función **con ERROR \_ INVALID \_ PARAMETER**.

Use la [**función ORCreateKey para**](orcreatekey.md) agregar claves a un subárbol del Registro sin conexión abierto y la función [**ORSetValue**](orsetvalue.md) para establecer los valores de las claves. La biblioteca del Registro sin conexión admite otras operaciones básicas del Registro, como enumerar, recuperar y eliminar claves y valores, y establecer atributos clave como la seguridad y el comportamiento de virtualización. Para obtener una lista de funciones, vea [Funciones de la biblioteca del Registro sin conexión](offline-registry-library-functions.md).

Para guardar los cambios realizados en un subárbol del Registro sin conexión abierto, use la [**función ORSaveHive**](orsavehive.md) para guardar el subárbol en un archivo. (Los cambios no se conservan a menos que se llame a **ORSaveHive).** Después de guardar el subárbol, use la [**función ORCloseHive**](orclosehive.md) para cerrar el subárbol y liberar recursos asociados a él.

Un subárbol del Registro sin conexión solo se valida cuando se abre mediante la [**función OROpenHive.**](oropenhive.md) Si el subárbol está dañado, la operación simplemente produce un error; no se ha intentado reparar el subárbol. Las comprobaciones de acceso en los objetos del subárbol no se realizan hasta que el subárbol se carga en un registro activo con la [función RegLoadKey.](/windows/win32/api/winreg/nf-winreg-regloadkeya)

Las funciones del Registro sin conexión no admiten [las claves predefinidas](../sysinfo/predefined-keys.md).

Todas las cadenas de nombre de clave y valor que se pasan a las funciones del Registro sin conexión deben ser Unicode.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Funciones de la biblioteca del Registro sin \_ conexión](offline-registry-library-functions.md)
</dt> </dl>

 

 
