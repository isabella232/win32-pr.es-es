---
description: 'Para crear una aplicación para WMI mediante C++: debe inicializar COM, tener acceso y establecer protocolos WMI y realizar una limpieza manual.'
ms.assetid: 0b9b7990-6982-4ba9-8dba-7470990405f7
ms.tgt_platform: multiple
title: Crear una aplicación WMI mediante C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6fc68bfb9b7c17967de3142c3e431b51fc340a32acfb94484030e8fe744bf067
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119612405"
---
# <a name="creating-a-wmi-application-using-c"></a>Crear una aplicación WMI mediante C++

Para crear una aplicación para WMI mediante C++: debe inicializar COM, tener acceso y establecer protocolos WMI y realizar una limpieza manual. Sin embargo, C++ tiene la ventaja de flexibilidad y potencia. Por lo tanto, aunque es mejor usar Visual Basic Scripting Edition (VBScript) o Windows PowerShell para procesos sencillos, C++ funciona mejor para aplicaciones más sofisticadas y es necesario para escribir proveedores [.](providing-data-to-wmi.md)

En el procedimiento siguiente se describe cómo crear una aplicación WMI.

**Para crear una aplicación WMI**

1.  [Inicialice COM](initializing-com-for-a-wmi-application.md).

    Dado que WMI se basa en la tecnología COM, debe realizar llamadas a las funciones [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) y [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) para acceder a WMI.

2.  [Cree una conexión a un espacio de nombres WMI.](creating-a-connection-to-a-wmi-namespace.md)

    Por definición, WMI se ejecuta en un proceso diferente al de la aplicación. Por lo tanto, debe crear una conexión entre la aplicación y WMI.

3.  [Establezca los niveles de seguridad en la conexión WMI.](setting-the-security-levels-on-a-wmi-connection.md)

    Para usar la conexión que cree a WMI, debe establecer los niveles de suplantación y autenticación de la aplicación.

4.  Implemente el propósito de la aplicación.

    WMI expone una variedad de interfaces COM que se usan para acceder a los datos y manipularlos en toda la empresa. Para obtener más información, vea [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md), Receiving a WMI [Event](receiving-a-wmi-event.md)y COM API [for WMI](com-api-for-wmi.md).

    Aquí es donde debe existir la mayor parte de la aplicación cliente WMI, como el acceso a objetos WMI o la manipulación de datos.

5.  [Limpie y apague la aplicación.](cleaning-up-and-shutting-down-a-wmi-application.md)

    Después de completar las consultas a WMI, debe destruir todos los punteros COM y apagar la aplicación correctamente.

Para obtener más información y un ejemplo de código sobre cómo crear una aplicación WMI, vea [Ejemplo: Crear una aplicación WMI.](example-creating-a-wmi-application.md)

 

 
