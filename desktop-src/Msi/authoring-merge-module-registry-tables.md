---
description: Use tablas del Registro de módulos de mezcla según el tipo de información del Registro.
ms.assetid: 091429ff-a8f4-4e1b-929f-1559cd173c3d
title: Creación de tablas del Registro de módulos de mezcla
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d10e31ac82d190c87019da5bc77408b58122a523
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159033"
---
# <a name="authoring-merge-module-registry-tables"></a>Creación de tablas del Registro de módulos de mezcla

Use tablas del Registro de módulos de mezcla según el tipo de información del Registro.

## <a name="typelib-class-appid-progid-extension-verb-or-mime-tables"></a>TypeLib, Class, AppId, ProgId, Extension, Verb o MIME Tables

Para bibliotecas de tipos, clases, extensiones y verbos, cree información del Registro en las tablas [TypeLib](typelib-table.md), [Class](class-table.md), [AppId](appid-table.md), [ProgId](progid-table.md), [Extension,](extension-table.md) [Verb](verb-table.md)o MIME del [módulo de](mime-table.md) mezcla. Si usa la tabla [Registro para](registry-table.md) agregar esta información, Windows 2000 no puede proporcionar anuncios de todo el sistema para estos componentes.

Los autores de módulos de mezcla pueden decidir no registrarse mediante la tabla Class por los siguientes motivos:

-   Para que la tabla Class lo registre, el archivo debe ser keyPath de su componente. Esto puede requerir un cambio inaceptable en la organización de los componentes.
-   Una llamada COM puede desencadenar un intento del instalador de reinstalar una clase anunciada. Los autores pueden decidir no registrar una clase mediante la tabla Class para evitar desencadenar una reinstalación cuando el equipo cliente no admite una interfaz de usuario.

## <a name="registry-table"></a>Tabla del Registro

Use la tabla Registry para agregar información del Registro que no se puede crear en las tablas TypeLib, Class, AppId, ProgId, Extension, Verb o MIME. Windows 2000 no puede proporcionar anuncios de todo el sistema para los componentes que usan la tabla del Registro.

Al crear la tabla del Registro, haga referencia a las rutas de acceso de archivo \[ \# mediante el archivo o \] \[ . Formato \] de archivo en lugar de nombre de archivo de \[ \] directorio. El último formato no admite la instalación desde el origen. El formato anterior también facilita la detección de archivos y componentes defectuosos.

Es necesario tener cuidado al usar texto con formato en la columna Clave de la tabla del Registro. Dado Windows instalador no vuelve a instalar los componentes que ya están instalados, el uso de texto con formato en este campo puede hacer que las claves del Registro se deban dejar atrás en la eliminación de la aplicación.

## <a name="selfreg-table"></a>Tabla SelfReg

No se recomienda usar la tabla SelfReg. Para obtener una lista de los motivos por los que no se usa el registro propio, consulte [la tabla SelfReg](selfreg-table.md). Debe usar las tablas TypeLib, Class, AppId, ProgId, Extension, Verb y MIME siempre que sea posible y la tabla Registry en todos los demás casos.

 

 



