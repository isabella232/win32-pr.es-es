---
description: 'Para crear una aplicación para WMI mediante C++: debe inicializar COM, obtener acceso y establecer los protocolos WMI y realizar una limpieza manual.'
ms.assetid: 0b9b7990-6982-4ba9-8dba-7470990405f7
ms.tgt_platform: multiple
title: Crear una aplicación WMI con C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: baaa4f7e79828b2cb6cb496254d906182ff611ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361280"
---
# <a name="creating-a-wmi-application-using-c"></a>Crear una aplicación WMI con C++

Para crear una aplicación para WMI mediante C++: debe inicializar COM, obtener acceso y establecer los protocolos WMI y realizar una limpieza manual. Sin embargo, C++ tiene la ventaja de flexibilidad y eficacia. Por lo tanto, aunque se puede atender mejor en el uso de Visual Basic Scripting Edition (VBScript) o Windows PowerShell para procesos sencillos, C++ funciona mejor para aplicaciones más sofisticadas y es necesario para escribir [proveedores](providing-data-to-wmi.md).

En el procedimiento siguiente se describe cómo crear una aplicación WMI.

**Para crear una aplicación WMI**

1.  [Inicializar com](initializing-com-for-a-wmi-application.md).

    Dado que WMI se basa en la tecnología COM, debe realizar llamadas a las funciones [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) y [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) para tener acceso a WMI.

2.  [Cree una conexión a un espacio de nombres WMI](creating-a-connection-to-a-wmi-namespace.md).

    Por definición, WMI se ejecuta en un proceso diferente del de la aplicación. Por lo tanto, debe crear una conexión entre la aplicación y WMI.

3.  [Establezca los niveles de seguridad en la conexión WMI](setting-the-security-levels-on-a-wmi-connection.md).

    Para usar la conexión que cree a WMI, debe establecer los niveles de suplantación y autenticación para la aplicación.

4.  Implemente el propósito de la aplicación.

    WMI expone una variedad de interfaces COM que se usan para obtener acceso a los datos de toda la empresa y manipularlos. Para obtener más información, vea [manipular información de clase e instancia](manipulating-class-and-instance-information.md), [recibir un evento WMI](receiving-a-wmi-event.md)y [API com para WMI](com-api-for-wmi.md).

    Aquí es donde debe existir la mayor parte de la aplicación cliente WMI, como el acceso a objetos WMI o la manipulación de datos.

5.  [Limpieza y cierre de la aplicación](cleaning-up-and-shutting-down-a-wmi-application.md).

    Después de completar las consultas en WMI, debe destruir todos los punteros COM y cerrar la aplicación correctamente.

Para obtener más información y un ejemplo de código sobre cómo crear una aplicación WMI, vea [ejemplo: crear una aplicación WMI](example-creating-a-wmi-application.md).

 

 
