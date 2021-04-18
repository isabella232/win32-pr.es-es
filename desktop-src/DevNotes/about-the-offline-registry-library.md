---
description: La biblioteca del registro sin conexión se utiliza para modificar un subárbol del registro fuera del registro del sistema activo.
ms.assetid: 61db2804-1b67-473f-8dd7-6be6c6a7184e
title: Acerca de la biblioteca de registro sin conexión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7e08b401a4a77f55a54c48ad147bf38c8796472
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104495893"
---
# <a name="about-the-offline-registry-library"></a>Acerca de la biblioteca de registro sin conexión

La biblioteca del registro sin conexión se utiliza para modificar un subárbol del registro fuera del registro del sistema activo.

La biblioteca del registro sin conexión está pensada para escenarios de actualización del registro, como el mantenimiento de una imagen de sistema operativo. Las funciones del registro sin conexión proporcionan las siguientes funcionalidades que no están disponibles con las funciones de registro estándar:

-   Las funciones del registro sin conexión se pueden usar para modificar un subárbol del registro en cualquier formato de registro compatible. Las funciones de registro estándar solo pueden realizar cambios en un subárbol del registro activo y los cambios deben ser compatibles con la versión de Windows que se ejecuta en el sistema.
-   La biblioteca del registro sin conexión solo requiere acceso de lectura para abrir un archivo de subárbol del registro y escribir el acceso para guardar el archivo. No se realiza ninguna otra comprobación de acceso en los objetos del subárbol, lo que permite modificar el subárbol con privilegios de usuario estándar. Con las funciones de registro estándar, cargar un subárbol en el registro activo es una operación con privilegios que requiere acceso administrativo.

Las funciones del registro sin conexión no se deben usar como sustituto de las funciones del registro del sistema por los siguientes motivos:

-   No es posible compartir subárboles del registro entre procesos mediante las funciones del registro sin conexión.
-   Las funciones del registro sin conexión usan un bloqueo simple que puede provocar una degradación seria del rendimiento de las aplicaciones multiproceso.
-   Los cambios realizados con las funciones del registro sin conexión no se guardan hasta que se llama a la función [**ORSaveHive**](orsavehive.md) .

Las aplicaciones no deben usar las funciones del registro sin conexión para omitir los requisitos de seguridad del registro del sistema. Para cargar un subárbol, una aplicación que se ejecuta sin los privilegios especiales que requiere la función [RegLoadKey](/windows/win32/api/winreg/nf-winreg-regloadkeya) puede usar la función [RegLoadAppKey](/windows/win32/api/winreg/nf-winreg-regloadappkeya) .

**Windows Server 2003 y Windows XP:** No se admite la función [RegLoadAppKey](/windows/win32/api/winreg/nf-winreg-regloadappkeya) .

Un *subárbol del registro sin conexión* es un subárbol del registro que se ha cargado en memoria mediante las funciones del registro sin conexión. Para crear un subárbol del registro sin conexión vacío, use la función [**ORCreateHive**](orcreatehive.md) . Para modificar un subárbol del registro existente, use la función [RegSaveKey](/windows/win32/api/winreg/nf-winreg-regsavekeya) o [RegSaveKeyEx](/windows/win32/api/winreg/nf-winreg-regsavekeyexa) para guardar un subárbol del registro del sistema activo en un archivo y, a continuación, use la función [**OROpenHive**](oropenhive.md) para abrir el archivo.

Las funciones [**ORCreateHive**](orcreatehive.md) y [**OROpenHive**](oropenhive.md) devuelven un identificador a la clave raíz del subárbol del registro sin conexión. Este identificador se puede usar como un identificador de cualquier otra clave del subárbol del registro sin conexión con las siguientes excepciones: las funciones [**ORCreateKey**](orcreatekey.md) y [**OROpenKey**](oropenkey.md) no se pueden usar para devolver un identificador a la clave raíz; no se puede usar la función [**ORCloseKey**](orclosekey.md) para cerrar la clave raíz; y la función [**ORDeleteKey**](ordeletekey.md) no se puede usar para eliminar la clave raíz. En todos estos casos, se produce un error en la función con un **\_ \_ parámetro no válido**.

Use la función [**ORCreateKey**](orcreatekey.md) para agregar claves a un subárbol del registro abierto sin conexión y a la función [**ORSetValue**](orsetvalue.md) para establecer los valores de las claves. La biblioteca del registro sin conexión admite otras operaciones básicas del registro, como enumerar, recuperar y eliminar claves y valores, y establecer atributos clave como la seguridad y el comportamiento de la virtualización. Para obtener una lista de funciones, consulte funciones de la [biblioteca del registro sin conexión](offline-registry-library-functions.md).

Para guardar los cambios realizados en un subárbol del registro abierto sin conexión, use la función [**ORSaveHive**](orsavehive.md) para guardar el subárbol en un archivo. (Los cambios no se conservan a menos que se llame a **ORSaveHive** ). Después de guardar el subárbol, use la función [**ORCloseHive**](orclosehive.md) para cerrar el subárbol y liberar los recursos asociados a él.

Un subárbol del registro sin conexión solo se valida cuando se abre con la función [**OROpenHive**](oropenhive.md) . Si el subárbol está dañado, simplemente se produce un error en la operación. no se realiza ningún intento de reparar el subárbol. Las comprobaciones de acceso en los objetos de Hive no se realizan hasta que el subárbol se carga en un registro activo con la función [RegLoadKey](/windows/win32/api/winreg/nf-winreg-regloadkeya) .

Las funciones del registro sin conexión no admiten las [claves predefinidas](../sysinfo/predefined-keys.md).

Todas las cadenas de nombre de valor y clave pasadas a las funciones del registro sin conexión deben ser Unicode.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Funciones de la biblioteca del registro sin conexión \_](offline-registry-library-functions.md)
</dt> </dl>

 

 
