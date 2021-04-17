---
description: Un proveedor de clases administra una clase o serie de clases para WMI.
ms.assetid: 755f1fde-a0bf-43f6-a01d-2da7d4e6c10d
ms.tgt_platform: multiple
title: Escribir un proveedor de clases
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff1e20115c4f833ad828e8d181ca97782d233130
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716188"
---
# <a name="writing-a-class-provider"></a>Escribir un proveedor de clases

Un proveedor de clases administra una clase o serie de clases para WMI. Un proveedor de clases puede ser de inserción o de extracción; es decir, puede almacenar sus propios datos o permitir a WMI almacenar datos para ellos en el servicio de administración de Windows. Aunque un proveedor de clases se instala en un equipo específico, puede cambiar las definiciones de clase en toda la empresa. Por lo tanto, la mayoría de los desarrolladores no suelen crear proveedores de clases.

Antes de construir un proveedor de clases, compruebe que las clases admitidas realmente se deben generar dinámicamente. En la mayoría de los casos, la lista de clases es de cambio lento y finita. Si es así, no debería tener que crear un proveedor de clases. En su lugar, puede colocar las definiciones de clase en el repositorio WMI mediante la API de WMI o un archivo MOF.

En el procedimiento siguiente se describe cómo implementar un proveedor de clases.

**Para implementar un proveedor de clases**

1.  Determine si el proveedor es un proveedor de inserción o de extracción.

    Un proveedor de extracción proporciona datos dinámicamente en respuesta a una solicitud de aplicación, mientras que los proveedores de inserción almacenan sus datos una vez en el repositorio WMI. Para obtener más información, vea [determinar el estado de inserción o extracción](determining-push-or-pull-status.md).

2.  Diseñe y registre el proveedor de clases con WMI.

    Los proveedores de clases se registran en WMI mediante la creación de una instancia de [**\_ \_ Win32Provider**](--win32provider.md) y una instancia de [**\_ \_ ClassProviderRegistration**](--classproviderregistration.md) . Para obtener más información, vea [registrar un proveedor de clases](registering-a-class-provider.md).

3.  Implemente la interfaz [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) para el proveedor.

    WMI usa [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) para cargar e inicializar un proveedor. Si está diseñando un proveedor de inserciones, **IWbemProviderInit** es la única interfaz que va a implementar. Para obtener más información, vea [inicializar un proveedor](initializing-a-provider.md).

    > [!Note]  
    > Se recomienda encarecidamente a los proveedores de clases que utilicen el modelo de multithreading "both".

     

4.  Agregue el código adicional necesario para el proveedor.

    Al diseñar el proveedor, lo más probable es que necesite llamar a interfaces de WMI. Para obtener más información, consulte [llamar a un método](calling-a-method.md) y [mantener los niveles de seguridad en un proveedor](impersonating-a-client.md).

    Al recuperar información de un cliente, es posible que necesite tener acceso a los niveles de seguridad de ese cliente. Para obtener más información, vea [Suplantar a un cliente](impersonating-a-client.md).

5.  Implemente la interfaz [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) para su proveedor.

    La interfaz [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) es la interfaz principal para un proveedor de clase de extracción. Para obtener más información, vea [implementar la interfaz principal para un proveedor de clases](implementing-the-primary-interface-for-a-class-provider.md).

6.  Reemplace el proveedor preexistente con el código nuevo.

    No es necesario que realice este paso si no tiene un proveedor preexistente en el que realizar la copia. Para obtener más información, consulte [actualización de un proveedor](updating-a-provider.md).

 

 



