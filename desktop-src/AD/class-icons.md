---
title: Iconos de clase
description: El icono que se usa para representar un objeto de clase se puede especificar en el atributo iconPath del contenedor DisplaySpecifiers.
ms.assetid: 0ff8da8a-d3d3-4a15-8103-4fe6ec307427
ms.tgt_platform: multiple
keywords:
- nombres para mostrar de clase AD, iconos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 691d4ef22babeded12ec9b951f92247df99521b6
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "103995102"
---
# <a name="class-icons"></a>Iconos de clase

El icono que se usa para representar un objeto de clase se puede especificar en el atributo **iconPath** del contenedor DisplaySpecifiers. Además, cada clase puede almacenar varios Estados de icono. Por ejemplo, una clase de carpeta puede tener iconos para los Estados abierto, cerrado y deshabilitado. La implementación actual acepta un máximo de dieciséis Estados de icono diferentes por clase.

El atributo **iconPath** se puede especificar de una de estas dos maneras.


```C++
<state>,<icon file name>
```



or


```C++
<state>,<module file name>,<resource ID>
```



En estos ejemplos, el " &lt; estado &gt; " es un entero con un valor comprendido entre 0 y 15. El valor 0 se define como el estado predeterminado o cerrado del icono. El valor 1 se define como el estado abierto del icono. El valor 2 es el Estado deshabilitado. Todos los demás valores están definidos por la aplicación.

El " &lt; nombre de archivo &gt; de icono" es la ruta de acceso y el nombre de un archivo de icono que contiene la imagen del icono.

El " &lt; nombre de archivo &gt; de módulo" es la ruta de acceso y el nombre de un módulo, como un archivo exe o dll, que contiene la imagen de icono en un recurso. El " &lt; identificador &gt; de recurso" es un entero que especifica el identificador de recurso del recurso de icono dentro del módulo.

## <a name="adding-a-value-to-the-iconpath-attribute"></a>Agregar un valor al atributo **iconPath**

Para agregar un valor al atributo **iconPath** , realice los pasos siguientes.

1.  Determine si el valor del atributo existe. Si un valor se va a reemplazar, elimine primero el valor existente mediante el método [**IADs::P Utex**](/windows/desktop/api/iads/nf-iads-iads-putex) con el parámetro *LnControlCode* establecido en **ADS \_ Property \_ Delete** y el parámetro *vProp* establecido en el valor que se va a quitar. No use la **\_ propiedad ADS \_ Clear** o la actualización de la **\_ propiedad \_ ADS** para *lnControlCode*.
2.  Cree la cadena que representa los datos del icono de atributo. Para obtener un ejemplo, vea el formato anterior.
3.  Para agregar el nuevo valor, use el método [**IADs::P Utex**](/windows/desktop/api/iads/nf-iads-iads-putex) con el parámetro *lnControlCode* establecido en la **propiedad de ADS \_ \_ Append**.
4.  Para confirmar los cambios en el directorio, llame a [**IADs:: SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo).

 

 