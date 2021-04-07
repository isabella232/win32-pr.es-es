---
description: Las aplicaciones pueden guardar parte del registro en un archivo y, a continuación, volver a cargar el contenido del archivo en el registro.
ms.assetid: a71a564d-934a-46e8-b555-989a6fa82337
title: Archivos de registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44916618946f6541495186aa5843799c9b864fbc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002129"
---
# <a name="registry-files"></a>Archivos de registro

Las aplicaciones pueden guardar parte del registro en un archivo y, a continuación, volver a cargar el contenido del archivo en el registro. Un archivo de registro es útil cuando se está manipulando una gran cantidad de datos, cuando se realizan muchas entradas en el registro, o cuando los datos son transitorios y se deben cargar y volver a cargar. Las aplicaciones que copian y restauran partes del registro probablemente usen archivos de registro.

Para guardar una clave y sus subclaves y valores en un archivo del registro, una aplicación puede llamar a la función [**RegSaveKey**](/windows/desktop/api/Winreg/nf-winreg-regsavekeya) o [**RegSaveKeyEx**](/windows/desktop/api/Winreg/nf-winreg-regsavekeyexa) .

[**RegSaveKey**](/windows/desktop/api/Winreg/nf-winreg-regsavekeya) y [**RegSaveKeyEx**](/windows/desktop/api/Winreg/nf-winreg-regsavekeyexa) crean el archivo con el atributo archive. El archivo se crea en el directorio actual del proceso para una clave local y en el directorio% SystemRoot% \\ system32 para una clave remota.

Los archivos de registro tienen los dos formatos siguientes: estándar y más reciente. El formato estándar es el único formato que admite Windows 2000. También se admite en versiones posteriores de Windows por compatibilidad con versiones anteriores. [**RegSaveKey**](/windows/desktop/api/Winreg/nf-winreg-regsavekeya) crea archivos en formato estándar.

El formato más reciente se admite a partir de Windows XP. Los archivos de registro que se crean con este formato no se pueden cargar en Windows 2000. [**RegSaveKeyEx**](/windows/desktop/api/Winreg/nf-winreg-regsavekeyexa) puede guardar archivos del registro en cualquiera de los dos formatos especificando el formato reg \_ estándar \_ o el \_ formato reg latest \_ . Por lo tanto, se puede usar para convertir los archivos de registro que usan el formato estándar al formato más reciente.

Para volver a escribir el archivo de registro en el registro, una aplicación puede usar las funciones [**RegLoadKey**](/windows/desktop/api/Winreg/nf-winreg-regloadkeya), [**RegReplaceKey**](/windows/desktop/api/Winreg/nf-winreg-regreplacekeya)o [**RegRestoreKey**](/windows/desktop/api/Winreg/nf-winreg-regrestorekeya) de la siguiente manera.

-   **RegLoadKey** carga los datos del registro de un archivo especificado en una subclave especificada en **HKEY \_ users** o **HKEY \_ local \_ Machine** en el equipo de la aplicación que realiza la llamada o en un equipo remoto. La función crea la subclave especificada si aún no existe. Después de llamar a esta función, una aplicación puede usar la función [**RegUnLoadKey**](/windows/desktop/api/Winreg/nf-winreg-regunloadkeya) para restaurar el registro a su estado anterior.
-   [**RegReplaceKey**](/windows/desktop/api/Winreg/nf-winreg-regreplacekeya) reemplaza una clave y todas sus subclaves y valores del registro por los datos contenidos en un archivo especificado. Los nuevos datos surtirán efecto la próxima vez que se inicie el sistema.
-   [**RegRestoreKey**](/windows/desktop/api/Winreg/nf-winreg-regrestorekeya) carga los datos del registro de un archivo especificado en una clave especificada en el equipo de la aplicación que realiza la llamada o en un equipo remoto. Esta función reemplaza las subclaves y valores por debajo de la clave especificada por las subclaves y los valores que siguen a la clave de nivel superior del archivo.

La función [**RegConnectRegistry**](/windows/desktop/api/Winreg/nf-winreg-regconnectregistrya) establece una conexión con un identificador de registro predefinido en otro equipo. Una aplicación usa esta función principalmente para tener acceso a información de un registro remoto en otros equipos de un entorno de red, lo que también se puede hacer mediante el editor del registro. Puede que desee tener acceso a un registro remoto para realizar una copia de seguridad de un registro o regular el acceso a la red. Tenga en cuenta que debe tener los permisos adecuados para tener acceso a un registro remoto mediante esta función.

 

 



