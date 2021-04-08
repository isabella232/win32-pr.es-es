---
title: Registrar la extensión de creación de objetos
description: Cuando se crea un archivo DLL de extensión de creación de objetos en Active Directory Domain Services, se debe registrar con el registro de Windows y Active Directory Domain Services para que COM y los complementos de MMC administrativos de Active Directory conozcan la extensión.
ms.assetid: 6e950c6c-1a4f-4de0-9be1-004c31d4734c
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c27d8e2a50c2340d678fd43e546d68525afbc8a7
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "103995064"
---
# <a name="registering-the-object-creation-extension"></a>Registrar la extensión de creación de objetos

Cuando se crea un archivo DLL de extensión de creación de objetos en Active Directory Domain Services, se debe registrar con el registro de Windows y Active Directory Domain Services para que COM y los complementos de MMC administrativos de Active Directory conozcan la extensión.

## <a name="registering-in-the-windows-registry"></a>Registro en el registro de Windows

Al igual que todos los servidores COM, una extensión de creación de objetos debe estar registrada en el registro de Windows. La extensión se registra con la siguiente clave:

```
HKEY_CLASSES_ROOT
   CLSID
      <extension CLSID>
         InProcServer32
            (Default) = <extension path>
            ThreadingModel = Apartment
```

" &lt; extensión CLSID &gt; " es la representación de cadena del CLSID tal y como la produce la función [**StringFromCLSID**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromclsid) . " &lt; ruta de acceso de la extensión &gt; " contiene la ruta de acceso y el nombre del archivo dll de extensión. El valor **ThreadingModel** para todas las extensiones de creación de objetos debe ser "Apartamento".

## <a name="registering-with-active-directory-domain-services"></a>Registro con Active Directory Domain Services

El registro de la extensión de creación de objetos es específico de una configuración regional. Si la extensión de creación de objetos se aplica a todas las configuraciones regionales, debe registrarse en el objeto **displaySpecifier** de la clase de objeto en todos los subcontenedores de la configuración regional del contenedor DisplaySpecifiers. Si la extensión de creación de objetos está localizada para una configuración regional determinada, regístrela en el objeto **displaySpecifier** en el subcontenedor de la configuración regional. Para obtener más información sobre el contenedor DisplaySpecifiers y las configuraciones regionales, consulte [especificadores de pantalla](display-specifiers.md) y [contenedor de DisplaySpecifiers](displayspecifiers-container.md).

Hay dos atributos DisplaySpecifier en los que se puede registrar una extensión de creación de objetos. Son **creationWizard** y **createWizardExt**.

El atributo **creationWizard** identifica las extensiones de creación de objetos principales para reemplazar el Asistente para creación de objetos existente o nativo en Active Directory complementos administrativos. Una extensión de creación principal proporciona el primer conjunto de páginas y se hospeda de la misma manera que las páginas nativas. Este atributo tiene un único valor y requiere el siguiente formato:


```C++
<CLSID>
```



El " &lt; CLSID &gt; " es la representación de cadena del CLSID del objeto com tal y como lo ha producido la función [**StringFromCLSID**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromclsid) .

El atributo **createWizardExt** identifica las extensiones de creación de objetos secundarios. Una extensión de creación secundaria agrega páginas del asistente a las páginas nativas o a la extensión principal. Este atributo tiene varios valores y requiere el siguiente formato:


```C++
<order number>,<CLSID>
```



El " &lt; número de pedido &gt; " es un número sin signo que representa la posición de la página en el asistente. Cuando se muestra un asistente para creación, los valores se ordenan mediante una comparación de "número de &lt; pedido" de cada valor &gt; . Si hay más de un valor con el mismo " &lt; número de pedido &gt; ", esas páginas se cargan en el orden en que se leen en el servidor de Active Directory. Si es posible, debe usar un " &lt; número de pedido" no existente &gt; (es decir, uno que no haya usado otros valores de la propiedad). No hay ninguna posición de inicio prescrita y se permiten huecos en la &lt; secuencia "número de pedido &gt; ".

El " &lt; CLSID &gt; " es la representación de cadena del CLSID del objeto com tal y como lo ha producido la función [**StringFromCLSID**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromclsid) .

 

 