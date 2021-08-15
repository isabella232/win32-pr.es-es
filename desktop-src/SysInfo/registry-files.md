---
description: Las aplicaciones pueden guardar parte del registro en un archivo y, a continuación, cargar el contenido del archivo de nuevo en el registro.
ms.assetid: a71a564d-934a-46e8-b555-989a6fa82337
title: Archivos del Registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3a5caa34a075e4bffe48a542d02eec896ab28dd93fbdc2745dbc5a08effb9d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117763818"
---
# <a name="registry-files"></a>Archivos del Registro

Las aplicaciones pueden guardar parte del registro en un archivo y, a continuación, cargar el contenido del archivo de nuevo en el registro. Un archivo del Registro es útil cuando se manipula una gran cantidad de datos, cuando se realizan muchas entradas en el registro o cuando los datos son transitorios y se deben cargar y volver a descargar. Es probable que las aplicaciones que copian y restauran partes del registro usen archivos del Registro.

Para guardar una clave y sus subclaves y valores en un archivo del Registro, una aplicación puede llamar a la [**función RegSaveKey**](/windows/desktop/api/Winreg/nf-winreg-regsavekeya) o [**RegSaveKeyEx.**](/windows/desktop/api/Winreg/nf-winreg-regsavekeyexa)

[**RegSaveKey y**](/windows/desktop/api/Winreg/nf-winreg-regsavekeya) [**RegSaveKeyEx**](/windows/desktop/api/Winreg/nf-winreg-regsavekeyexa) crean el archivo con el atributo archive. El archivo se crea en el directorio actual del proceso para una clave local y en el directorio %systemroot% \\ system32 para una clave remota.

Los archivos del Registro tienen los dos formatos siguientes: estándar y más reciente. El formato estándar es el único formato admitido por Windows 2000. También es compatible con versiones posteriores de Windows compatibilidad con versiones anteriores. [**RegSaveKey crea**](/windows/desktop/api/Winreg/nf-winreg-regsavekeya) archivos en el formato estándar.

El formato más reciente se admite a partir de Windows XP. Los archivos del Registro que se crean en este formato no se pueden cargar Windows 2000. [**RegSaveKeyEx puede**](/windows/desktop/api/Winreg/nf-winreg-regsavekeyexa) guardar los archivos del Registro en cualquier formato especificando REG \_ STANDARD FORMAT o REG LATEST \_ \_ \_ FORMAT. Por lo tanto, se puede usar para convertir los archivos del Registro que usan el formato estándar al formato más reciente.

Para volver a escribir el archivo del Registro en el Registro, una aplicación puede usar las funciones [**RegLoadKey**](/windows/desktop/api/Winreg/nf-winreg-regloadkeya), [**RegReplaceKey**](/windows/desktop/api/Winreg/nf-winreg-regreplacekeya)o [**RegRestoreKey**](/windows/desktop/api/Winreg/nf-winreg-regrestorekeya) como se muestra a continuación.

-   **RegLoadKey carga** los datos del Registro de un archivo especificado en una subclave especificada en **HKEY \_ USERS** o **HKEY \_ LOCAL \_ MACHINE** en el equipo de la aplicación que realiza la llamada o en un equipo remoto. La función crea la subclave especificada si aún no existe. Después de llamar a esta función, una aplicación puede usar [**la función RegUnLoadKey**](/windows/desktop/api/Winreg/nf-winreg-regunloadkeya) para restaurar el registro a su estado anterior.
-   [**RegReplaceKey**](/windows/desktop/api/Winreg/nf-winreg-regreplacekeya) reemplaza una clave y todas sus subclaves y valores del Registro por los datos contenidos en un archivo especificado. Los nuevos datos se verán efectivos la próxima vez que se inicia el sistema.
-   [**RegRestoreKey carga**](/windows/desktop/api/Winreg/nf-winreg-regrestorekeya) los datos del Registro de un archivo especificado en una clave especificada en el equipo de la aplicación que realiza la llamada o en un equipo remoto. Esta función reemplaza las subclaves y los valores situados debajo de la clave especificada por las subclaves y los valores que siguen a la clave de nivel superior del archivo.

La [**función RegConnectRegistry**](/windows/desktop/api/Winreg/nf-winreg-regconnectregistrya) establece una conexión a un identificador del Registro predefinido en otro equipo. Una aplicación usa esta función principalmente para acceder a información de un registro remoto en otras máquinas de un entorno de red, lo que también puede hacer mediante el Editor del Registro. Es posible que quiera acceder a un registro remoto para hacer una copia de seguridad de un registro o regular el acceso de red a él. Tenga en cuenta que debe tener los permisos adecuados para acceder a un registro remoto mediante esta función.

 

 



