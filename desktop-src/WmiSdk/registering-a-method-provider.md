---
description: Para crear un proveedor de métodos WMI, debe registrar la \_ \_ instancia de Win32Provider que representa el proveedor mediante una instancia de \_ \_ MethodProviderRegistration.
ms.assetid: 1cfb16ae-8dcf-437d-b779-db2f30bb0d34
ms.tgt_platform: multiple
title: Registrar un proveedor de métodos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a399f90c6fc6f97e9ada8051055505b43885da3b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277697"
---
# <a name="registering-a-method-provider"></a>Registrar un proveedor de métodos

Para crear un [*proveedor de métodos*](gloss-m.md) WMI, debe registrar la instancia de [**\_ \_ Win32Provider**](--win32provider.md) que representa el proveedor mediante una instancia de [**\_ \_ MethodProviderRegistration**](--methodproviderregistration.md). Después de crear una instancia de [**\_ \_ Win32Provider**](--win32provider.md), debe registrar ese proveedor con WMI. Como objeto COM, el proveedor debe registrarse en el sistema operativo y en WMI. En el procedimiento siguiente se supone que ya ha implementado el proceso de registro como se describe en [registrar un proveedor](registering-a-provider.md).

En el procedimiento siguiente se describe cómo registrar un proveedor de métodos.

**Para registrar un proveedor de métodos**

1.  Cree una instancia de la clase [**\_ \_ Win32Provider**](--win32provider.md) que describa el proveedor.

    La clase del sistema [**\_ \_ MethodProviderRegistration**](--methodproviderregistration.md) hereda muchas propiedades de la clase primaria [**\_ \_ ObjectProviderRegistration**](--objectproviderregistration.md) , sin embargo, la única propiedad pertinente para un proveedor de métodos es la ruta de acceso del objeto a la instancia de [**\_ \_ Win32Provider**](--win32provider.md) .

2.  Cree una instancia de la clase [**\_ \_ MethodProviderRegistration**](--methodproviderregistration.md) que describa el conjunto de características del proveedor.

    Asegúrese de etiquetar la clase con los calificadores de [**proveedor**](/windows/desktop/api/Provider/nl-provider-provider) y [**dinámicos**](dynamic-qualifier.md) . El calificador **dinámico** indica que WMI debe utilizar un proveedor para recuperar las instancias de clase. El calificador de **proveedor** especifica el nombre del proveedor que debe usar WMI.

En el ejemplo de código siguiente se describe cómo registrar un proveedor de métodos.

``` syntax
  instance of __Win32Provider as $P
  {
    Name    = "MethProvider" ;
    ClsId   = "{E30EC6A0-23CF-11d1-8FDE-0000F804AA5C}" ;
  };    

  instance of __MethodProviderRegistration
  {
    Provider = $P;
  };
```

 

 



