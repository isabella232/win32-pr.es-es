---
title: Registrar el objeto COM del menú contextual en un especificador de presentación
description: En este tema se muestran las claves del registro que deben modificarse para registrar un objeto COM de menú contextual.
ms.assetid: 389bc249-4849-4763-9d1b-b35598a51050
ms.tgt_platform: multiple
keywords:
- Registrar el objeto COM del menú contextual en un especificador de presentación
- menú contextual AD (objeto), registrar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62ae30c1a60a1a0bc5a8ec388a3578ab13829c95
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "104077499"
---
# <a name="registering-the-context-menu-com-object-in-a-display-specifier"></a>Registrar el objeto COM del menú contextual en un especificador de presentación

Cuando se usa COM para crear un archivo DLL de extensión de menú contextual para un servicio de directorio de Active Directory, la extensión se debe registrar con el registro de Windows y Active Directory Domain Services para notificar a los Active Directory complementos de MMC administrativos y el shell de Windows de la extensión.

## <a name="registering-in-the-windows-registry"></a>Registro en el registro de Windows

Al igual que todos los servidores COM, se debe registrar una extensión de menú contextual en el registro. La extensión se registra con la siguiente clave.

```
HKEY_CLASSES_ROOT
   CLSID
      <clsid>
```

*<clsid>* es la representación de cadena del CLSID tal y como la produce la función [**StringFromCLSID**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromclsid) . En la *<clsid>* clave, hay una clave **InProcServer32** que identifica el objeto como servidor de 32 bits en proceso. En la clave **InProcServer32** , la ubicación del archivo dll se especifica en el valor predeterminado y el modelo de subprocesos se especifica en el valor **ThreadingModel** . Todas las extensiones del menú contextual deben usar el modelo de subprocesos "Apartamento".

## <a name="registering-with-active-directory-domain-services"></a>Registro con Active Directory Domain Services

El registro de la extensión del menú contextual es específico de una configuración regional. Si la extensión del menú contextual se aplica a todas las configuraciones regionales, debe registrarse en el objeto [**displaySpecifier**](/windows/desktop/ADSchema/c-displayspecifier) de la clase de objeto en todos los subcontenedores de la configuración regional en el contenedor de especificadores de presentación. Si la extensión del menú contextual se localiza para una configuración regional determinada, se debe registrar en el objeto **displaySpecifier** en el subcontenedor de la configuración regional. Para obtener más información sobre el contenedor de especificadores de presentación y configuraciones regionales, vea [especificadores de pantalla](display-specifiers.md) y [contenedor de DisplaySpecifiers](displayspecifiers-container.md).

Hay dos atributos de especificador de presentación en los que se puede registrar un elemento de extensión de menú contextual. Son [**adminContextMenu**](/windows/desktop/ADSchema/a-admincontextmenu) y [**shellContextMenu**](/windows/desktop/ADSchema/a-shellcontextmenu).

El atributo [**adminContextMenu**](/windows/desktop/ADSchema/a-admincontextmenu) identifica los menús contextuales administrativos que se van a mostrar en Active Directory complementos administrativos. El menú contextual aparece cuando el usuario muestra el menú contextual de los objetos de la clase adecuada en una de las Active Directory complementos administrativos de MMC.

El atributo [**shellContextMenu**](/windows/desktop/ADSchema/a-shellcontextmenu) identifica los menús contextuales del usuario final que se van a mostrar en el shell de Windows. El menú contextual aparece cuando el usuario ve el menú contextual de los objetos de la clase adecuada en el explorador de Windows. A partir de Windows Server 2003, el shell de Windows ya no muestra objetos de Active Directory Domain Services.

Todos estos atributos tienen varios valores.

Al registrar una extensión de menú contextual, los valores de los atributos [**adminContextMenu**](/windows/desktop/ADSchema/a-admincontextmenu) y [**shellContextMenu**](/windows/desktop/ADSchema/a-shellcontextmenu) requieren el formato siguiente.


```C++
<order number>,<clsid>
```



El " &lt; número &gt; de pedido" es un número sin signo que representa la posición del elemento en el menú contextual. Cuando se muestra un menú contextual, los valores se ordenan mediante una comparación de "número de &lt; pedido" de cada valor &gt; . Si hay más de un valor con el mismo " &lt; número de pedido &gt; ", esas extensiones del menú contextual se cargan en el orden en que se leen en el servidor de Active Directory. Si es posible, use un "número de &lt; pedido" no existente &gt; , es decir, uno que no haya usado otros valores de la propiedad. No hay ninguna posición de inicio prescrita y se permiten brechas en la &lt; secuencia "número de pedido &gt; ".

" &lt; CLSID &gt; " es la representación de cadena del CLSID tal y como la produce la función [**StringFromCLSID**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromclsid) .

En el shell de Windows, se admiten los elementos de menú contextual de selección múltiple. En este caso, la extensión del menú contextual se invoca para cada objeto seleccionado. En Active Directory complementos administrativos, también se admiten los elementos de extensión del menú contextual de selección múltiple. En este caso, la estructura [**DSOBJECTNAMES**](/windows/desktop/api/Dsclient/ns-dsclient-dsobjectnames) contendrá una estructura [**DSOBJECT**](/windows/desktop/api/Dsclient/ns-dsclient-dsobject) para cada objeto de directorio seleccionado.

> [!IMPORTANT]
> En el shell de Windows, la información del especificador de presentación se recupera en el inicio de sesión del usuario y se almacena en caché para la sesión del usuario. En el caso de los complementos administrativos, los datos del especificador de presentación se recuperan cuando se carga el complemento y se almacenan en memoria caché mientras dure el proceso. En el caso del shell de Windows, esto significa que los cambios en los especificadores de presentación surten efecto después de que un usuario cierre la sesión y vuelva a iniciarla. En el caso de los complementos administrativos, los cambios surten efecto cuando se vuelve a cargar el complemento o el archivo de consola, es decir, si se inicia una nueva instancia del archivo de consola o una nueva instancia de Mmc.exe y se agrega el complemento, se recuperan los datos del especificador de pantalla más reciente.

 

Para obtener más información y un ejemplo de código sobre cómo implementar una extensión de menú contextual, vea [código de ejemplo para la implementación del objeto com del menú contextual](example-code-for-implementation-of-the-context-menu-com-object.md).

 

 