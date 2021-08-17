---
description: Un proveedor de clases administra una clase o serie de clases para WMI.
ms.assetid: 755f1fde-a0bf-43f6-a01d-2da7d4e6c10d
ms.tgt_platform: multiple
title: Escribir un proveedor de clases
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b45815c795b6f43f3e7ec99b9ce9535c4d14b2bc8426ea5ca6b44f736415bbf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118311944"
---
# <a name="writing-a-class-provider"></a>Escribir un proveedor de clases

Un proveedor de clases administra una clase o serie de clases para WMI. Un proveedor de clases puede ser de inserción o extracción; es decir, puede almacenar sus propios datos o permitir que WMI almacene datos para ellos en el servicio Windows administración de archivos. Aunque un proveedor de clases está instalado en un equipo específico, puede cambiar las definiciones de clase en toda una empresa. Por lo tanto, la mayoría de los desarrolladores no suelen crear proveedores de clases.

Antes de construir un proveedor de clases, compruebe que las clases admitidas realmente se deben generar dinámicamente. En la mayoría de los casos, la lista de clases es de cambio lento y finito. Si este es el caso, no debe tener que crear un proveedor de clases. En su lugar, puede colocar las definiciones de clase en el repositorio WMI mediante la API wmi o un archivo MOF.

En el procedimiento siguiente se describe cómo implementar un proveedor de clases.

**Para implementar un proveedor de clases**

1.  Determine si el proveedor es un proveedor de inserción o extracción.

    Un proveedor de extracción proporciona datos dinámicamente en respuesta a una solicitud de aplicación, mientras que los proveedores de inserción almacenan sus datos una vez en el repositorio WMI. Para obtener más información, vea [Determinar el estado de inserción o extracción.](determining-push-or-pull-status.md)

2.  Diseñe y registre el proveedor de clases con WMI.

    Los proveedores de clases se registran con WMI mediante la creación de una [**\_ \_ instancia de Win32Provider**](--win32provider.md) y una [**\_ \_ instancia classProviderRegistration.**](--classproviderregistration.md) Para obtener más información, [vea Registrar un proveedor de clases](registering-a-class-provider.md).

3.  Implemente [**la interfaz IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) para el proveedor.

    WMI usa [**IWbemProviderInit para**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) cargar e inicializar un proveedor. Si va a diseñar un proveedor de inserción, **IWbemProviderInit** es la única interfaz que implementará. Para obtener más información, vea [Inicializar un proveedor.](initializing-a-provider.md)

    > [!Note]  
    > Se recomienda encarecidamente a los proveedores de clases que usen el modelo multithreading "Both".

     

4.  Agregue cualquier código adicional necesario para el proveedor.

    Al diseñar el proveedor, lo más probable es que deba llamar a interfaces WMI. Para obtener más información, vea [Llamar a un método y](calling-a-method.md) Mantener niveles de seguridad en un [proveedor](impersonating-a-client.md).

    Al recuperar información para un cliente, es posible que tenga que acceder a los niveles de seguridad de ese cliente. Para obtener más información, [vea Suplantar un cliente.](impersonating-a-client.md)

5.  Implemente [**la interfaz IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) para el proveedor.

    La [**interfaz IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) es la interfaz principal de un proveedor de clases de extracción. Para obtener más información, vea [Implementar la interfaz principal para un proveedor de clases](implementing-the-primary-interface-for-a-class-provider.md).

6.  Reemplace el proveedor existente por el nuevo código.

    No es necesario realizar este paso si no tiene un proveedor preexistnte sobre el que copiar. Para obtener más información, vea [Actualizar un proveedor](updating-a-provider.md).

 

 



