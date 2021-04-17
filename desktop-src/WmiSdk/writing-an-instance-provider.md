---
description: Un proveedor de instancias proporciona instancias de una o varias clases determinadas.
ms.assetid: d53c3399-cba8-4b5d-8da0-b5a23f94c0ae
ms.tgt_platform: multiple
title: Escribir un proveedor de instancias
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72bddfaa867624bd84cc975d32a8e7b747064d1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706558"
---
# <a name="writing-an-instance-provider"></a>Escribir un proveedor de instancias

Un proveedor de instancias proporciona instancias de una o varias clases determinadas. Por ejemplo, un proveedor de instancias puede proporcionar información relacionada con una CPU u otro tipo de hardware. Dado que los objetos administrados por un proveedor de instancias tienden a cambiar periódicamente, todos los proveedores de instancias se consideran proveedores de extracción; es decir, un proveedor que recupera dinámicamente información relacionada con un objeto administrado siempre que WMI realiza una solicitud de la información. El nombre proviene de la idea de que WMI "extrae" la información del proveedor en nombre de una solicitud de cliente. Con la tecnología de extracción, un proveedor de instancias puede admitir la recuperación, enumeración, modificación, eliminación y procesamiento de consultas de una instancia específica.

Los proveedores de alto rendimiento pueden aumentar la eficacia de un proveedor de instancias o tener acceso mediante programación a los datos que aparecen en el monitor de sistema. Para obtener más información, vea [crear un proveedor de instancias en un proveedor de High-Performance](making-an-instance-provider-into-a-high-performance-provider.md).

En el procedimiento siguiente se describe cómo escribir un proveedor de instancias.

**Para escribir un proveedor de instancias**

1.  [Registre el proveedor con WMI](registering-an-instance-provider.md).

    Los proveedores de instancias se registran en WMI mediante la creación de una instancia de [**\_ \_ Win32Provider**](--win32provider.md) y una clase [**\_ \_ InstanceProviderRegistration**](--instanceproviderregistration.md) .

2.  [Inicialice el proveedor](initializing-a-provider.md).

    WMI usa [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) para cargar e inicializar un proveedor. Se trata de una tarea común a todos los proveedores.

    > [!Note]  
    > Se recomienda encarecidamente a los proveedores de instancias que utilicen el modelo de multithreading "both".

     

3.  [Implemente la interfaz IWbemServices para su proveedor](implementing-the-primary-interface-for-an-instance-provider.md).

    La interfaz [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) es la interfaz principal para un proveedor de instancias.

4.  Agregue el código adicional necesario para el proveedor.

    Al diseñar el proveedor, lo más probable es que necesite llamar a interfaces de WMI. Para obtener más información, consulte [realizar llamadas a WMI](making-calls-to-wmi.md).

    Al recuperar información de un cliente, es posible que necesite tener acceso a los niveles de seguridad de ese cliente. Para obtener más información, vea [Suplantar a un cliente](impersonating-a-client.md).

5.  Si es necesario, [implemente la interfaz de alto rendimiento](improving-the-efficiency-of-an-instance-provider.md).

    La interfaz de alto rendimiento aumenta la velocidad a la que el proveedor puede reaccionar ante las solicitudes de WMI.

6.  Si es necesario, [implemente la compatibilidad con las actualizaciones de instancias parciales](supporting-partial-instance-operations.md).

    Como su nombre implica, una actualización de instancia parcial es una técnica que se usa para actualizar solo parte de una instancia. Para obtener más información sobre cómo llamar a una instancia parcial desde un cliente, vea [Actualizar parte de una instancia](updating-part-of-an-instance.md) y [recuperar parte de una instancia de WMI](retrieving-part-of-an-instance.md).

7.  Reemplace el proveedor preexistente con el código nuevo.

    No es necesario que realice este paso si no tiene un proveedor preexistente en el que realizar la copia. Para obtener más información, consulte [actualización de un proveedor](updating-a-provider.md).

 

 



