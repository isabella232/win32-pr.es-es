---
description: Para crear un proveedor de propiedades WMI, debe registrar la \_ \_ instancia de Win32Provider que representa el proveedor mediante una instancia de \_ \_ PropertyProviderRegistration.
ms.assetid: e7e30acc-ea41-41e2-9bb3-cd931e8d799e
ms.tgt_platform: multiple
title: Registrar un proveedor de propiedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d56d91e3c2a45b0ad0fe83cf6b2bc32ab4353a26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276147"
---
# <a name="registering-a-property-provider"></a>Registrar un proveedor de propiedades

Para crear un [*proveedor de propiedades*](gloss-p.md) WMI, debe registrar la instancia de [**\_ \_ Win32Provider**](--win32provider.md) que representa el proveedor mediante una instancia de [**\_ \_ PropertyProviderRegistration**](--propertyproviderregistration.md). Como objeto COM, el proveedor debe registrarse en el sistema operativo y en WMI. En el procedimiento siguiente se supone que ya ha implementado el proceso de registro como se describe en [registrar un proveedor](registering-a-provider.md).

En el procedimiento siguiente se describe cómo registrar un proveedor de propiedades.

**Para registrar un proveedor de propiedades**

1.  Cree una instancia de la clase [**\_ \_ Win32Provider**](--win32provider.md) que describa el proveedor de propiedades.

    La clase [**\_ \_ Win32Provider**](--win32provider.md) acepta los valores predeterminados para otras propiedades, como el valor **true** para la propiedad **Pure** . Para obtener más información, vea [**\_ \_ Win32Provider**](--win32provider.md).

2.  Cree una instancia de la clase [**\_ \_ PropertyProviderRegistration**](--propertyproviderregistration.md) que describa el conjunto de características del proveedor.

    La clase [**\_ \_ PropertyProviderRegistration**](--propertyproviderregistration.md) hereda muchas propiedades de la clase primaria [**\_ \_ ObjectProviderRegistration**](--objectproviderregistration.md) , que proporciona valores booleanos que indican la compatibilidad con características concretas y una matriz de cadenas para indicar la compatibilidad con consultas.

    Asegúrese de etiquetar la clase con los calificadores de [**proveedor**](/windows/desktop/api/Provider/nl-provider-provider) y [**dinámicos**](dynamic-qualifier.md) . El calificador **dinámico** indica que WMI debe utilizar un proveedor dinámico para recuperar las instancias de clase que contienen las propiedades admitidas. El calificador de **proveedor** especifica el nombre del proveedor que debe usar WMI.

WMI llama a NewQuery en un proveedor de eventos cuando un consumidor de cliente registra una consulta de filtro de eventos que contiene referencias a eventos admitidos por ese proveedor de eventos. Por lo tanto, el proveedor de eventos responsable de los eventos de modificación de instancias de la clase EmailClass puede configurarse para generar notificaciones solo para el remitente. Cuando el proveedor recibe una consulta que solicita la notificación de los cambios en la propiedad de asunto, el proveedor puede empezar a generar esas notificaciones. En este escenario, no se requiere WMI para descartar las notificaciones que solo notifican los cambios de destinatarios.

En el siguiente ejemplo de código MOF se describen las instancias de que se pueden utilizar para registrar un proveedor de propiedades.

``` syntax
  instance of __Win32Provider as $P
  {
    Name    = "PropProvider" ;
    ClsId   = "{E30EC6A0-23CF-11d1-8FDE-0000F804AA5C}" ;
  };    

  instance of __PropertyProviderRegistration
  {
    Provider = $P;
    SupportsGet = TRUE;
    SupportsPut = FALSE;
  };
```

> [!Note]  
> Solo los administradores pueden registrar o eliminar un proveedor de propiedades mediante la creación de una instancia de [**\_ \_ Win32Provider**](--win32provider.md) y [**\_ \_ PropertyProviderRegistration**](--propertyproviderregistration.md).

 

 

 



