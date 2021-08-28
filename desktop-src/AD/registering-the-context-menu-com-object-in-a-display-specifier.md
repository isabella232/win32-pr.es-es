---
title: Registrar el objeto COM del menú contextual en un especificador de presentación
description: En este tema se muestran las claves del Registro que deben modificarse para registrar un objeto COM de menú contextual.
ms.assetid: 389bc249-4849-4763-9d1b-b35598a51050
ms.tgt_platform: multiple
keywords:
- Registrar el objeto COM del menú contextual en un especificador de presentación
- objeto COM del menú contextual de AD, registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c5650d5864093293728e5c4f1157980c76bffa0
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122881249"
---
# <a name="registering-the-context-menu-com-object-in-a-display-specifier"></a>Registrar el objeto COM del menú contextual en un especificador de presentación

Cuando se usa COM para crear un archivo DLL de extensión de menú contextual para un servicio de directorio de Active Directory, la extensión se debe registrar con el Registro de Windows y Active Directory Domain Services para notificar Active Directory los complementos MMC administrativos y el shell Windows de la extensión.

## <a name="registering-in-the-windows-registry"></a>Registro en el registro Windows registro

Al igual que todos los servidores COM, se debe registrar una extensión de menú contextual en el Registro. La extensión se registra con la clave siguiente.

```
HKEY_CLASSES_ROOT
   CLSID
      <clsid>
```

*&lt; clsid &gt;* es la representación de cadena del CLSID que genera la [**función StringFromCLSID.**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromclsid) En la *&lt; clave &gt; clsid,* hay una clave **InProcServer32** que identifica el objeto como un servidor en proceso de 32 bits. En la **clave InProcServer32,** la ubicación del archivo DLL se especifica en el valor predeterminado y el modelo de subprocesos se especifica en el **valor ThreadingModel.** Toda la extensión del menú contextual debe usar el modelo de subprocesos "Apartment".

## <a name="registering-with-active-directory-domain-services"></a>Registro con Active Directory Domain Services

El registro de la extensión del menú contextual es específico de una configuración regional. Si la extensión de menú contextual se aplica a todas las configuraciones regionales, debe registrarse en la clase de objeto [**displaySpecifier**](/windows/desktop/ADSchema/c-displayspecifier) en todos los subcontenedores de configuración regional del contenedor Display Specifiers. Si la extensión de menú contextual se localiza para una configuración regional determinada, debe registrarse en el objeto **displaySpecifier** en el subcontenedor de esa configuración regional. Para obtener más información sobre el contenedor display specifiers y las configuraciones regionales, vea [Display Specifiers](display-specifiers.md) and [DisplaySpecifiers Container](displayspecifiers-container.md).

Hay dos atributos de especificador de presentación en los que se puede registrar un elemento de extensión de menú contextual. Estos son [**adminContextMenu**](/windows/desktop/ADSchema/a-admincontextmenu) y [**shellContextMenu.**](/windows/desktop/ADSchema/a-shellcontextmenu)

El [**atributo adminContextMenu**](/windows/desktop/ADSchema/a-admincontextmenu) identifica los menús contextuales administrativos que se mostrarán Active Directory complementos administrativos. El menú contextual aparece cuando el usuario muestra el menú contextual de los objetos de la clase adecuada en uno de los Active Directory complementos MMC administrativos.

El [**atributo shellContextMenu**](/windows/desktop/ADSchema/a-shellcontextmenu) identifica los menús contextuales del usuario final que se mostrarán en Windows shell. El menú contextual aparece cuando el usuario ve el menú contextual de los objetos de la clase adecuada en Windows Explorer. A partir Windows Server 2003, el shell de Windows ya no muestra objetos de Active Directory Domain Services.

Todos estos atributos tienen varios valores.

Al registrar una extensión de menú contextual, los valores de los atributos [**adminContextMenu**](/windows/desktop/ADSchema/a-admincontextmenu) y [**shellContextMenu**](/windows/desktop/ADSchema/a-shellcontextmenu) requieren el formato siguiente.


```C++
<order number>,<clsid>
```



" order number " es un número sin signo &lt; que representa la posición del elemento en el menú &gt; contextual. Cuando se muestra un menú contextual, los valores se ordenan mediante una comparación del "número de orden" &lt; de cada &gt; valor. Si más de un valor tiene el mismo "número de pedido", esas extensiones de menú contextual se cargan en el orden en que &lt; &gt; se leen desde Active Directory servidor. Si es posible, use un número de pedido "no existente", es decir, uno que otros valores de la propiedad no hayan &lt; &gt; usado. No hay ninguna posición inicial prescrita y se permiten espacios en la secuencia &lt; "número de &gt; pedido".

" clsid " es la representación de cadena del CLSID que genera &lt; &gt; la función [**StringFromCLSID.**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromclsid)

En el shell Windows, se admiten elementos de menú contextual de selección múltiple. En este caso, se invoca la extensión de menú contextual para cada objeto seleccionado. En Active Directory complementos administrativos, también se admiten elementos de extensión de menú contextual de selección múltiple. En este caso, la [**estructura DSOBJECTNAMES**](/windows/desktop/api/Dsclient/ns-dsclient-dsobjectnames) contendrá una estructura [**DSOBJECT**](/windows/desktop/api/Dsclient/ns-dsclient-dsobject) para cada objeto de directorio seleccionado.

> [!IMPORTANT]
> Para el Windows, la información del especificador para mostrar se recupera al iniciar sesión del usuario y se almacena en caché para la sesión del usuario. Para los complementos administrativos, los datos del especificador de visualización se recuperan cuando se carga el complemento y se almacenan en caché mientras dura el proceso. En el Windows shell, esto significa que los cambios para mostrar especificadores tienen efecto después de que un usuario cierra sesión y vuelve a intentarlo. En el caso de los complementos administrativos, los cambios tienen efecto cuando se vuelve a cargar el complemento o el archivo de consola, es decir, si inicia una nueva instancia del archivo de consola o una nueva instancia de Mmc.exe y agrega el complemento, se recuperan los datos del especificador de visualización más recientes.

 

Para obtener más información y un ejemplo de código de cómo implementar una extensión de menú contextual, vea Código de ejemplo para la implementación del objeto [COM del menú contextual](example-code-for-implementation-of-the-context-menu-com-object.md).

 

 
