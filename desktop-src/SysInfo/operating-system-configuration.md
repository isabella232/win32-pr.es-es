---
description: El Windows directorio es el directorio que contiene aplicaciones basadas Windows, archivos de inicialización y archivos de ayuda. La función GetWindowsDirectory recupera la ruta de acceso a este directorio.
ms.assetid: c07c6337-2c92-42c5-8283-c95637fcb85a
title: Configuración del sistema operativo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a38aa2c2b6b4f6b3ac5caac78a89ad980a9bd074
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073514"
---
# <a name="operating-system-configuration"></a>Configuración del sistema operativo

El *Windows directorio es* el directorio que contiene aplicaciones basadas Windows, archivos de inicialización y archivos de ayuda. La [**función GetWindowsDirectory**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getwindowsdirectorya) recupera la ruta de acceso a este directorio.

El *directorio del sistema* es el directorio que contiene bibliotecas de vínculos dinámicos, controladores y archivos de fuentes. La [**función GetSystemDirectory**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemdirectorya) recupera la ruta de acceso a este directorio.

La [**función GetUserName**](/windows/desktop/api/Winbase/nf-winbase-getusernamea) recupera el nombre del usuario que ha iniciado sesión actualmente en el sistema. El nombre de usuario es el nombre de inicio de sesión o el nombre completo del usuario, si este último se incluye en el registro.

Una *variable de entorno* es una variable simbólica que representa algún elemento del sistema, como una ruta de acceso, un nombre de archivo u otros datos literales. Por ejemplo, la variable de entorno PATH representa los directorios en los que se buscarán archivos ejecutables. Cuando un usuario inicia sesión, el sistema inicializa variables de entorno en función de la sección de entorno del Registro. La [**función ExpandEnvironmentStrings**](/windows/win32/api/processenv/nf-processenv-expandenvironmentstringsa) recupera los valores de las variables de entorno especificadas.

La interfaz [**IADsADSystemInfo**](/windows/desktop/api/iads/nn-iads-iadsadsysteminfo) proporciona información adicional.

 

 
