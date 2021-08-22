---
title: Registrar un elemento de menú contextual estático
description: En este tema se describe el registro de un elemento de menú contextual estático que se muestra para Active Directory objetos.
ms.assetid: ed945812-3adb-4058-bdb6-8d9d34468265
ms.tgt_platform: multiple
keywords:
- Registro de un elemento de menú contextual estático AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26e34d2ed02a4f30702ca91551b5b7f5c9dc3e2d1294faae043054be047031b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118184514"
---
# <a name="registering-a-static-context-menu-item"></a>Registrar un elemento de menú contextual estático

Los complementos MMC administrativos de Active Directory Domain Services y el shell de Windows proporcionan un mecanismo para agregar un elemento al menú contextual que se muestra para los objetos de Active Directory Domain Services. El menú contextual puede invocar cualquier archivo que se pueda iniciar con [**shellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) API, como una dirección URL de aplicación o página web.

## <a name="registering-with-active-directory-domain-services"></a>Registro con Active Directory Domain Services

El registro de la extensión del menú contextual es específico de una configuración regional. Si la extensión de menú contextual se aplica a todas las configuraciones regionales, debe registrarse en la clase de objeto [**displaySpecifier**](/windows/desktop/ADSchema/c-displayspecifier) en todos los subcontenedores de configuración regional del contenedor Display Specifiers. Si la extensión de menú contextual está localizada para una configuración regional determinada, debe registrarse en el **objeto displaySpecifier** de ese subcontenedor de configuración regional. Para obtener más información sobre el contenedor display specifiers y las configuraciones regionales, vea [Display Specifiers](display-specifiers.md) and [DisplaySpecifiers Container](displayspecifiers-container.md).

Hay dos atributos de especificador de presentación en los que se puede registrar un elemento de menú contextual estático, [**adminContextMenu**](/windows/desktop/ADSchema/a-admincontextmenu) [**y shellContextMenu.**](/windows/desktop/ADSchema/a-shellcontextmenu)

El [**atributo adminContextMenu**](/windows/desktop/ADSchema/a-admincontextmenu) identifica los menús contextuales administrativos que se muestran en los complementos administrativos de Active Directory Domain Services. El menú contextual aparece cuando el usuario muestra el menú contextual de los objetos de la clase adecuada en uno de los complementos MMC administrativos.

El [**atributo shellContextMenu**](/windows/desktop/ADSchema/a-shellcontextmenu) identifica los menús contextuales del usuario final que se mostrarán en Windows shell. El menú contextual aparece cuando el usuario ve el menú contextual de los objetos de la clase adecuada en Windows Explorer. A partir de Windows Server 2003, el shell de Windows ya no muestra objetos que son de Active Directory Domain Services.

Todos estos atributos tienen varios valores.

Al registrar un elemento de menú contextual estático, los valores de los atributos [**adminContextMenu**](/windows/desktop/ADSchema/a-admincontextmenu) y [**shellContextMenu**](/windows/desktop/ADSchema/a-shellcontextmenu) requieren el formato siguiente.


```C++
<order number>,<menu text>,<command>
```



" order number " es un número sin signo que representa la posición del elemento &lt; &gt; en el menú contextual. Cuando se muestra un menú contextual, los valores se ordenan mediante una comparación del "número de pedido" &lt; de cada &gt; valor. Si más de un valor tiene el mismo "número de pedido", esas extensiones de menú contextual se cargan en el orden en que &lt; &gt; se leen desde Active Directory servidor. Si es posible, use un número de pedido "no existente", es decir, uno que otros valores de la propiedad no hayan &lt; &gt; usado. No hay ninguna posición inicial prescrita y se permiten espacios en la secuencia &lt; "número de &gt; pedido".

El texto &lt; del menú " es la cadena que se muestra en el menú &gt; contextual. El texto &lt; del menú "" puede incluir un carácter "&" que precede al carácter de método abreviado de &gt; teclado para el elemento de menú. Esto hará que se subrayado el carácter anterior. Por ejemplo, si el "texto del menú " es "&File", el texto del menú se mostrará como &lt; "File", la "F" se subraya y "F" será el método abreviado de teclado para el elemento de &gt; menú.

El comando &lt; " " es el programa o archivo ejecutado por el &gt; complemento. Debe especificarse la ruta de acceso completa o el archivo debe existir en la variable de entorno de ruta de acceso del equipo. El archivo se invoca mediante la [**función ShellExecute.**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) El comando " &lt; " no puede contener parámetros &gt; adicionales, por ejemplo, Notepad.exe Myfile.txt. Dado **que se usa ShellExecute,** cualquier archivo o dirección que se pueda pasar a **ShellExecute** se puede usar para el &lt; comando &gt; ". Por ejemplo, si el comando " contiene &lt; &gt; "d: \\file.txt", d:file.txt se abrirá con la aplicación asociada a la \\ .txt extensión. Del mismo modo, si el comando " contiene " ", se abre el explorador web predeterminado &lt; y se mostrará la página web &gt; https://www.fabrikam.com especificada. Se permiten rutas de acceso y nombres de aplicación con espacios. Si " &lt; command " es una aplicación, la clase YDsPath y la clase del objeto seleccionado se pasan como argumentos de línea de &gt; comandos, separados por un espacio.

En el shell Windows, se admiten elementos de menú contextual de selección múltiple. En este caso, se invoca &lt; el comando " para cada objeto &gt; seleccionado. En Active Directory Domain Services complementos administrativos, no se admiten elementos de menú contextual estático de selección múltiple.

> [!IMPORTANT]
> Para el Windows, los datos del especificador para mostrar se recuperan en el inicio de sesión del usuario y se almacenan en caché para la sesión del usuario. Para los complementos administrativos, los datos del especificador de visualización se recuperan cuando se carga el complemento y se almacenan en caché mientras dura el proceso. Para el Windows shell, esto significa que los cambios en los especificadores de visualización tienen efecto después de que un usuario cierra sesión y vuelve a intentarlo. En el caso de los complementos administrativos, los cambios tienen efecto cuando se vuelve a cargar el complemento o el archivo de consola; Es decir, si inicia una nueva instancia del archivo de consola o una nueva instancia de Mmc.exe y agrega el complemento, se recuperan los datos del especificador de visualización más recientes.

 

Para obtener más información y un ejemplo de código, vea [Ejemplo de código para instalar un elemento de menú contextual estático.](example-code-for-installing-a-static-context-menu-item.md)

 

 