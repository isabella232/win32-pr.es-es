---
title: Registro de un elemento de menú contextual estático
description: En este tema se describe el registro de un elemento de menú contextual estático que se muestra para Active Directory objetos.
ms.assetid: ed945812-3adb-4058-bdb6-8d9d34468265
ms.tgt_platform: multiple
keywords:
- Registro de un elemento de menú contextual estático AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89e3ee5336061ca296e2c94f8907ebd385610494
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "105656325"
---
# <a name="registering-a-static-context-menu-item"></a>Registro de un elemento de menú contextual estático

Los complementos MMC administrativos de Active Directory Domain Services y el shell de Windows proporcionan un mecanismo para agregar un elemento al menú contextual que se muestra para los objetos de Active Directory Domain Services. El menú contextual puede invocar cualquier archivo que se pueda iniciar con la API de [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) , como una aplicación o una dirección URL de la Página Web.

## <a name="registering-with-active-directory-domain-services"></a>Registro con Active Directory Domain Services

El registro de la extensión del menú contextual es específico de una configuración regional. Si la extensión del menú contextual se aplica a todas las configuraciones regionales, debe registrarse en el objeto [**displaySpecifier**](/windows/desktop/ADSchema/c-displayspecifier) de la clase de objeto en todos los subcontenedores de la configuración regional en el contenedor de especificadores de presentación. Si la extensión del menú contextual está localizada para una configuración regional determinada, se debe registrar en el objeto **displaySpecifier** en el subcontenedor de la configuración regional. Para obtener más información sobre el contenedor de especificadores de presentación y configuraciones regionales, vea [especificadores de pantalla](display-specifiers.md) y [contenedor de DisplaySpecifiers](displayspecifiers-container.md).

Hay dos atributos de especificador de presentación en los que se puede registrar un elemento de menú contextual estático, [**adminContextMenu**](/windows/desktop/ADSchema/a-admincontextmenu) y [**shellContextMenu**](/windows/desktop/ADSchema/a-shellcontextmenu).

El atributo [**adminContextMenu**](/windows/desktop/ADSchema/a-admincontextmenu) identifica los menús contextuales administrativos que se van a mostrar en los complementos administrativos de Active Directory Domain Services. El menú contextual aparece cuando el usuario muestra el menú contextual de los objetos de la clase adecuada en uno de los complementos MMC administrativos.

El atributo [**shellContextMenu**](/windows/desktop/ADSchema/a-shellcontextmenu) identifica los menús contextuales del usuario final que se van a mostrar en el shell de Windows. El menú contextual aparece cuando el usuario ve el menú contextual de los objetos de la clase adecuada en el explorador de Windows. A partir de Windows Server 2003, el shell de Windows ya no muestra los objetos que provienen de Active Directory Domain Services.

Todos estos atributos tienen varios valores.

Al registrar un elemento de menú contextual estático, los valores de los atributos [**adminContextMenu**](/windows/desktop/ADSchema/a-admincontextmenu) y [**shellContextMenu**](/windows/desktop/ADSchema/a-shellcontextmenu) requieren el formato siguiente.


```C++
<order number>,<menu text>,<command>
```



El " &lt; número de pedido &gt; " es un número sin signo que representa la posición del elemento en el menú contextual. Cuando se muestra un menú contextual, los valores se ordenan mediante una comparación de "número de &lt; pedido" de cada valor &gt; . Si hay más de un valor con el mismo " &lt; número de pedido &gt; ", esas extensiones del menú contextual se cargan en el orden en que se leen en el servidor de Active Directory. Si es posible, use un "número de &lt; pedido" no existente &gt; , es decir, uno que no haya usado otros valores de la propiedad. No hay ninguna posición de inicio prescrita y se permiten huecos en la &lt; secuencia "número de pedido &gt; ".

El " &lt; texto del menú &gt; " es la cadena que se muestra en el menú contextual. El " &lt; texto de menú &gt; " puede incluir un carácter "&" que precede al carácter de método abreviado de teclado para el elemento de menú. Esto hará que el carácter precedido esté subrayado. Por ejemplo, si el " &lt; texto del menú &gt; " es "&archivo", el texto del menú se mostrará como "archivo", la "f" se subrayará y "f" será el método abreviado de teclado para el elemento de menú.

El " &lt; comando &gt; " es el programa o archivo ejecutado por el complemento. Se debe especificar la ruta de acceso completa o el archivo debe existir en la variable de entorno de ruta de acceso del equipo. El archivo se invoca mediante la función [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) . El " &lt; comando &gt; " no puede contener parámetros adicionales, por ejemplo, Notepad.exe Myfile.txt. Dado que se utiliza **ShellExecute** , cualquier archivo o dirección que se pueda pasar a **ShellExecute** se puede usar para " &lt; Command &gt; ". Por ejemplo, si " &lt; comando &gt; " contiene "d: \\file.txt", d: \\file.txt se abrirá con la aplicación asociada a la extensión. txt. Del mismo modo, si " &lt; comando &gt; " contiene " https://www.fabrikam.com ", se abrirá el explorador Web predeterminado y se mostrará la Página Web especificada. Se permiten las rutas de acceso y los nombres de aplicación con espacios. Si &lt; el "comando &gt; " es una aplicación, el ADsPath y la clase del objeto seleccionado se pasan como argumentos de la línea de comandos, separados por un espacio.

En el shell de Windows, se admiten los elementos de menú contextual de selección múltiple. En este caso, &lt; se invoca el "comando &gt; " para cada objeto seleccionado. En Active Directory Domain Services no se admiten los elementos de menú contextual estático de selección múltiple.

> [!IMPORTANT]
> En el shell de Windows, los datos del especificador de presentación se recuperan al iniciar sesión el usuario y se almacenan en caché para la sesión del usuario. En el caso de los complementos administrativos, los datos del especificador de presentación se recuperan cuando se carga el complemento y se almacenan en memoria caché mientras dure el proceso. En el caso del shell de Windows, esto significa que los cambios en los especificadores de presentación surten efecto después de que un usuario cierre la sesión y vuelva a iniciarla. En el caso de los complementos administrativos, los cambios surten efecto cuando se recarga el complemento o el archivo de consola. es decir, si inicia una nueva instancia del archivo de consola o una nueva instancia de Mmc.exe y agrega el complemento, se recuperan los datos del especificador de pantalla más reciente.

 

Para obtener más información y un ejemplo de código, vea [código de ejemplo para instalar un elemento de menú contextual estático](example-code-for-installing-a-static-context-menu-item.md).

 

 