---
description: Use tablas del registro del módulo de mezcla según el tipo de información del registro.
ms.assetid: 091429ff-a8f4-4e1b-929f-1559cd173c3d
title: Crear tablas del registro del módulo de combinación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d10e31ac82d190c87019da5bc77408b58122a523
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001729"
---
# <a name="authoring-merge-module-registry-tables"></a>Crear tablas del registro del módulo de combinación

Use tablas del registro del módulo de mezcla según el tipo de información del registro.

## <a name="typelib-class-appid-progid-extension-verb-or-mime-tables"></a>Tablas TypeLib, clase, AppId, ProgId, extensión, verbo o MIME

En el caso de las bibliotecas de tipos, las clases, las extensiones y los verbos, cree información del registro en las tablas [typelib](typelib-table.md), [Class](class-table.md), [AppID](appid-table.md), [ProgID](progid-table.md), [Extension](extension-table.md), [Verb](verb-table.md)o [MIME](mime-table.md) del módulo de combinación. Si usa la [tabla del registro](registry-table.md) para agregar esta información, Windows 2000 no puede proporcionar anuncios para estos componentes en todo el sistema.

Los autores del módulo de combinación pueden decidir no registrarse mediante la tabla de clases por los siguientes motivos:

-   Para que la tabla de clases registre la clase, el archivo debe ser la ruta de acceso de su componente. Esto puede requerir un cambio inaceptable en la organización de los componentes.
-   Una llamada COM puede desencadenar un intento de instalación de la reinstalación de una clase anunciada. Los autores pueden decidir no registrar una clase mediante la tabla de clases con el fin de evitar la activación de una reinstalación cuando el equipo cliente no admite una interfaz de usuario.

## <a name="registry-table"></a>Tabla del registro

Use la tabla del registro para agregar información del registro que no se puede crear en las tablas TypeLib, Class, AppId, ProgId, Extension, Verb o MIME. Windows 2000 no puede proporcionar un anuncio para todo el sistema para los componentes que utilizan la tabla del registro.

Al crear la tabla del registro, consulte las rutas de acceso de archivo con el \[ \# archivo \] o \[ ! \]Formato de archivo en lugar de un nombre de archivo de \[ directorio \] . El último formato no admite la instalación de ejecución desde el origen. El formato anterior también hace que los archivos que faltan y los componentes defectuosos sean más fáciles de detectar.

Se necesita atención cuando se usa texto con formato en la columna de clave de la tabla del registro. Dado que Windows Installer no reinstala los componentes que ya están instalados, el uso de texto con formato en este campo puede hacer que las claves del registro queden detrás de la eliminación de la aplicación.

## <a name="selfreg-table"></a>Tabla SelfReg

No se recomienda usar la tabla SelfReg. Para obtener una lista de razones para no utilizar el registro automático, consulte [tabla SelfReg](selfreg-table.md). En su lugar, debe usar las tablas TypeLib, Class, AppId, ProgId, Extension, Verb y MIME, siempre que sea posible, y la tabla del registro en todos los demás casos.

 

 



