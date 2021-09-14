---
description: Para crear un proveedor de métodos WMI, debe registrar la instancia de Win32Provider que representa al proveedor mediante una instancia \_ \_ \_ \_ de MethodProviderRegistration.
ms.assetid: 1cfb16ae-8dcf-437d-b779-db2f30bb0d34
ms.tgt_platform: multiple
title: Registrar un proveedor de métodos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a399f90c6fc6f97e9ada8051055505b43885da3b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127241659"
---
# <a name="registering-a-method-provider"></a>Registrar un proveedor de métodos

Para crear un proveedor [*de métodos*](gloss-m.md) WMI, debe registrar la instancia [**\_ \_ de Win32Provider**](--win32provider.md) que representa al proveedor mediante una instancia de [**\_ \_ MethodProviderRegistration**](--methodproviderregistration.md). Después de crear una instancia [**\_ \_ de Win32Provider,**](--win32provider.md)debe registrar ese proveedor con WMI. Como objeto COM, el proveedor debe registrarse con el sistema operativo y WMI. En el procedimiento siguiente se da por supuesto que ya ha implementado el proceso de registro como se describe [en Registro de un proveedor](registering-a-provider.md).

En el procedimiento siguiente se describe cómo registrar un proveedor de métodos.

**Para registrar un proveedor de métodos**

1.  Cree una instancia de la [**\_ \_ clase Win32Provider**](--win32provider.md) que describa el proveedor.

    La clase del sistema [**\_ \_ MethodProviderRegistration**](--methodproviderregistration.md) hereda muchas propiedades de la clase primaria [**\_ \_ ObjectProviderRegistration;**](--objectproviderregistration.md) sin embargo, la única propiedad relevante para un proveedor de métodos es la ruta de acceso del objeto a la instancia [**\_ \_ de Win32Provider.**](--win32provider.md)

2.  Cree una instancia de la [**\_ \_ clase MethodProviderRegistration**](--methodproviderregistration.md) que describa el conjunto de características del proveedor.

    Asegúrese de etiquetar la clase con los calificadores [**Dynamic**](dynamic-qualifier.md) [**y Provider.**](/windows/desktop/api/Provider/nl-provider-provider) El **calificador** Dinámico indica que WMI debe usar un proveedor para recuperar las instancias de clase. El **calificador** Provider especifica el nombre del proveedor que WMI debe usar.

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

 

 



