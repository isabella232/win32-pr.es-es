---
description: Las variables de entorno especifican rutas de búsqueda para archivos, directorios para archivos temporales, opciones específicas de la aplicación y otra información similar.
ms.assetid: 6180e54e-4bd9-4692-83fd-f3f7f1d8f8d7
title: Variables de entorno de usuario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf4f898c7a9135c0421fdd67a7bed1d97655556f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127574500"
---
# <a name="user-environment-variables"></a>Variables de entorno de usuario

Las variables de entorno especifican rutas de búsqueda para archivos, directorios para archivos temporales, opciones específicas de la aplicación y otra información similar. El sistema mantiene un bloque de entorno para cada usuario y uno para el equipo. El bloque de entorno del sistema representa variables de entorno para todos los usuarios del equipo en particular. El bloque de entorno de un usuario representa las variables de entorno que mantiene el sistema para ese usuario determinado, incluido el conjunto de variables de entorno del sistema.

De forma predeterminada, cada proceso recibe una copia del bloque de entorno para su proceso primario. Normalmente, este es el bloque de entorno para el usuario que ha iniciado sesión. Un proceso puede especificar distintos bloques de entorno para sus procesos secundarios mediante las funciones [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) [**o CreateProcessAsUser.**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera)

Para agregar o modificar variables de entorno, el usuario selecciona **Sistema** en la Panel de control **y,** a continuación, selecciona la **pestaña** Entorno. El usuario también puede agregar o modificar variables de entorno en un símbolo del sistema mediante el **comando set.** Las variables de entorno creadas **con el comando set** solo se aplican a la ventana de comandos en la que se establecen y a sus procesos secundarios. Para obtener más información, escriba **set /?** en un símbolo del sistema.

Para recuperar una copia del bloque de entorno para un usuario determinado, use la [**función CreateEnvironmentBlock.**](/windows/desktop/api/Userenv/nf-userenv-createenvironmentblock) Para liberar un bloque de entorno creado **por CreateEnvironmentBlock,** use la [**función DestroyEnvironmentBlock.**](/windows/desktop/api/Userenv/nf-userenv-destroyenvironmentblock) Estas funciones hacen referencia a un puntero a un bloque de entorno. El bloque de entorno es una matriz de cadenas Unicode terminadas en NULL. La lista termina con dos valores NULL ( \\ 0 \\ 0).

Para expandir una cadena que contiene variables de entorno mediante el bloque de entorno para un usuario especificado, use la función [**ExpandEnvironmentStringsForUser.**](/windows/desktop/api/Userenv/nf-userenv-expandenvironmentstringsforusera)

 

 
