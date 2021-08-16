---
title: Iconos de clase
description: El icono utilizado para representar un objeto de clase se puede especificar en el atributo iconPath del contenedor DisplaySpecifiers.
ms.assetid: 0ff8da8a-d3d3-4a15-8103-4fe6ec307427
ms.tgt_platform: multiple
keywords:
- nombres para mostrar de clase AD ,icons
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efe3548daa223cdfa05dee8ec3df8f2f8bc800c5ba7449920744de1a67ac8745
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118022606"
---
# <a name="class-icons"></a>Iconos de clase

El icono utilizado para representar un objeto de clase se puede especificar en el **atributo iconPath** del contenedor DisplaySpecifiers. Además, cada clase puede almacenar varios estados de icono. Por ejemplo, una clase de carpeta puede tener iconos para los estados abierto, cerrado y deshabilitado. La implementación actual acepta un máximo de 16 estados de icono diferentes por clase.

El **atributo iconPath** se puede especificar de una de estas dos maneras.


```C++
<state>,<icon file name>
```



o


```C++
<state>,<module file name>,<resource ID>
```



En estos ejemplos, el &lt; "estado &gt; " es un entero con un valor entre 0 y 15. El valor 0 se define como el estado predeterminado o cerrado del icono. El valor 1 se define para que sea el estado abierto del icono. El valor 2 es el estado deshabilitado. Todos los demás valores están definidos por la aplicación.

"nombre de archivo de icono" es la ruta de acceso y el nombre de archivo de un &lt; archivo de icono que contiene la imagen de &gt; icono.

"Nombre de archivo de módulo" es la ruta de acceso y el nombre de archivo de un módulo, como un archivo EXE o DLL, que contiene la imagen de &lt; &gt; icono de un recurso. El &lt; "id. de recurso" es un entero que especifica el identificador de &gt; recurso del recurso de icono dentro del módulo.

## <a name="adding-a-value-to-the-iconpath-attribute"></a>Agregar un valor al **atributo iconPath**

Para agregar un valor al atributo **iconPath,** realice los pasos siguientes.

1.  Determine si el valor del atributo existe. Si se va a reemplazar un valor, elimine primero el valor existente mediante el método [**IADs::P utEx**](/windows/desktop/api/iads/nf-iads-iads-putex) con el parámetro *lnControlCode* establecido en **ADS PROPERTY \_ \_ DELETE** y el parámetro *vProp* establecido en el valor que se va a quitar. No use **ADS PROPERTY CLEAR \_ \_ o** **ADS PROPERTY \_ \_ UPDATE** para *lnControlCode*.
2.  Cree la cadena que representa los datos del icono de atributo. Para obtener un ejemplo, vea el formato anterior.
3.  Para agregar el nuevo valor, use el método [**IADs::P utEx**](/windows/desktop/api/iads/nf-iads-iads-putex) con el parámetro *lnControlCode* establecido en **ADS PROPERTY \_ \_ APPEND**.
4.  Para confirmar los cambios en el directorio, llame [**a IADs::SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo).

 

 