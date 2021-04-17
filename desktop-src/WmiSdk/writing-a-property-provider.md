---
description: Un proveedor de propiedades recupera y modifica los valores de propiedad individuales para las instancias de una clase determinada que se almacena en el repositorio WMI.
ms.assetid: fe150157-cf9d-47da-8f94-b18eb0502bd8
ms.tgt_platform: multiple
title: Escribir un proveedor de propiedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06bf22d927435b5c46f0ec8d8d2cf42ab872a0c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716187"
---
# <a name="writing-a-property-provider"></a>Escribir un proveedor de propiedades

Un proveedor de propiedades recupera y modifica los valores de propiedad individuales para las instancias de una clase determinada que se almacena en el repositorio WMI.

En el procedimiento siguiente se describe cómo crear un proveedor de propiedades.

**Para crear un proveedor de propiedades**

1.  Diseñe y registre el proveedor con WMI.

    Los proveedores de instancias se registran en WMI mediante la creación de una instancia de [**\_ \_ Win32Provider**](--win32provider.md) y una clase [**\_ \_ PropertyProviderRegistration**](--propertyproviderregistration.md) . Para obtener más información, vea [registrar un proveedor de propiedades](registering-a-property-provider.md).

2.  Implemente la interfaz [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) para el proveedor.

    WMI usa [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) para cargar e inicializar un proveedor. Se trata de una tarea común a todos los proveedores. Para obtener más información, vea [inicializar un proveedor](initializing-a-provider.md).

    > [!Note]  
    > Se recomienda encarecidamente a los proveedores de propiedades que utilicen el modelo de multithreading "both".

     

3.  Implemente la interfaz [**IWbemPropertyProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbempropertyprovider) para el proveedor.

    La interfaz [**IWbemPropertyProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbempropertyprovider) es la interfaz principal para un proveedor de propiedades. Los dos métodos principales son [**GetProperty**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbempropertyprovider-getproperty) y [**PutProperty**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbempropertyprovider-putproperty). Para obtener más información, vea [implementar la interfaz principal para un proveedor de propiedades](implementing-the-primary-interface-for-a-property-provider.md).

4.  Agregue el código adicional necesario para el proveedor.

    Al diseñar el proveedor, lo más probable es que necesite llamar a interfaces de WMI. Para obtener más información, consulte [llamar a un método](calling-a-method.md) y [mantener los niveles de seguridad en un proveedor](impersonating-a-client.md).

    Al recuperar información de un cliente, es posible que necesite tener acceso a los niveles de seguridad de ese cliente. Para obtener más información, vea [Suplantar a un cliente](impersonating-a-client.md).

5.  Reemplace el proveedor preexistente con el código nuevo.

    No es necesario que realice este paso si no tiene un proveedor preexistente en el que realizar la copia. Para obtener más información, consulte [actualización de un proveedor](updating-a-provider.md).

 

 



