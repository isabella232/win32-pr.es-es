---
description: Para crear un proveedor de propiedades WMI, debe registrar la instancia de Win32Provider que representa al proveedor mediante una instancia \_ \_ de \_ \_ PropertyProviderRegistration.
ms.assetid: e7e30acc-ea41-41e2-9bb3-cd931e8d799e
ms.tgt_platform: multiple
title: Registro de un proveedor de propiedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d56d91e3c2a45b0ad0fe83cf6b2bc32ab4353a26
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127063926"
---
# <a name="registering-a-property-provider"></a>Registro de un proveedor de propiedades

Para crear un proveedor [*de propiedades*](gloss-p.md) WMI, debe registrar la instancia [**\_ \_ de Win32Provider**](--win32provider.md) que representa al proveedor mediante una instancia de [**\_ \_ PropertyProviderRegistration**](--propertyproviderregistration.md). Como objeto COM, el proveedor debe registrarse con el sistema operativo y WMI. En el procedimiento siguiente se da por supuesto que ya ha implementado el proceso de registro como se describe en [Registro de un proveedor.](registering-a-provider.md)

En el procedimiento siguiente se describe cómo registrar un proveedor de propiedades.

**Para registrar un proveedor de propiedades**

1.  Cree una instancia de la [**\_ \_ clase Win32Provider**](--win32provider.md) que describa el proveedor de propiedades.

    La [**\_ \_ clase Win32Provider**](--win32provider.md) acepta los valores predeterminados para otras propiedades, como el **valor TRUE** para la **propiedad Pure.** Para obtener más información, [**\_ \_ vea Win32Provider**](--win32provider.md).

2.  Cree una instancia de la [**\_ \_ clase PropertyProviderRegistration**](--propertyproviderregistration.md) que describa el conjunto de características del proveedor.

    La [**\_ \_ clase PropertyProviderRegistration**](--propertyproviderregistration.md) hereda muchas propiedades de la clase primaria [**\_ \_ ObjectProviderRegistration,**](--objectproviderregistration.md) que proporciona valores booleanos que indican la compatibilidad con características concretas y una matriz de cadenas para indicar la compatibilidad con consultas.

    Asegúrese de etiquetar la clase con los calificadores [**Dynamic**](dynamic-qualifier.md) [**y Provider.**](/windows/desktop/api/Provider/nl-provider-provider) El **calificador** Dinámico indica que WMI debe usar un proveedor dinámico para recuperar las instancias de clase que contienen las propiedades admitidas. El **calificador** Provider especifica el nombre del proveedor que WMI debe usar.

WMI llama a NewQuery en un proveedor de eventos cuando un consumidor cliente registra una consulta de filtro de eventos que contiene referencias a eventos compatibles con ese proveedor de eventos. Por lo tanto, el proveedor de eventos responsable de los eventos de modificación de instancias de la clase EmailClass se puede configurar para generar notificaciones solo para el remitente. Cuando el proveedor recibe una consulta que solicita la notificación de cambios en la propiedad subject, el proveedor puede empezar a generar esas notificaciones. En este escenario, WMI no tiene que descartar las notificaciones que informan de que el destinatario solo cambia.

En el ejemplo de código MOF siguiente se describen las instancias que se pueden usar para registrar un proveedor de propiedades.

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

 

 

 



