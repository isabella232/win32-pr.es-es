---
title: Modificar interfaces de usuario existentes
description: El panel de resultados del Usuarios y equipos de Active Directory complemento MMC muestra varias columnas de datos de atributos para objetos dentro de un contenedor, como los atributos Nombre y Descripción.
ms.assetid: 55f4ae82-c380-42a9-beba-047ffd0131eb
ms.tgt_platform: multiple
keywords:
- Modificación de las interfaces de usuario existentes de AD
- Complemento Usuarios y equipos de AD, modificación de la pantalla
- Complemento Usuarios y equipos de AD, agregar columnas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dcf6ef4743009086ae19148c42a8addc5974e4ac833cdad8eee675fdce76a5f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025873"
---
# <a name="modifying-existing-user-interfaces"></a>Modificar interfaces de usuario existentes

El panel de resultados del Usuarios y equipos de Active Directory complemento MMC muestra varias columnas de datos de atributos para objetos dentro de un contenedor, como los atributos **Nombre** **y** Descripción. El complemento permite al usuario agregar y quitar las columnas que se muestran en el panel de resultados del complemento.

Para cambiar la pantalla, el usuario usa **el** menú desplegable Ver y selecciona Agregar o **quitar columnas.** En el **cuadro de diálogo** Agregar o quitar columnas , hay una lista de columnas que el usuario puede elegir para mostrar en el panel de resultados.

El complemento MMC de Usuarios y equipos de Active Directory que se incluye con Windows Server 2003, Standard Edition, Windows Server 2003, Enterprise Edition y Windows Server 2003, Datacenter Edition, proporciona la capacidad de modificar la lista de columnas que se pueden mostrar en el panel de resultados del complemento para un contenedor. Esta característica solo existe si el complemento está destinado a un bosque con Windows esquema de Server 2003.

Para agregar una columna a la lista, agregue un valor al atributo **extraColumns** del especificador de visualización para el tipo de objeto al que está asociado el atributo. El **atributo extraColumns** es un atributo de cadena multivalor donde cada cadena tiene el formato siguiente.


```C++

<ldapdisplayname>,<column header>,<default visibility>,<width>,<unused>

```



En la tabla siguiente se muestra el contenido de estos valores.



| Value                        | Descripción                                                                                                                         |
|------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| " &lt; ldapdisplayname &gt; "    | Contiene una cadena que representa **el ldapDisplayName** del atributo.                                                         |
| " &lt; encabezado de columna &gt; "      | Contiene una cadena que representa el texto mostrado en el encabezado de la columna.                                                  |
| " &lt; visibilidad predeterminada &gt; " | Contiene un valor numérico que es 0 si el atributo está oculto de forma predeterminada o 1 si el atributo está visible de forma predeterminada.               |
| " &lt; width &gt; "              | Contiene el ancho de la columna, en píxeles. Si este valor es -1, el ancho de la columna se establece en el ancho del encabezado de columna. |
| " &lt; sin usar &gt; "             | Sin usar. Debe ser cero.                                                                                                               |



 

Por ejemplo, para agregar una columna que mostrará el nombre canónico de los objetos de una unidad organizativa, se agrega un valor para el atributo **canonicalName** al atributo **extraColumns** del objeto **organizationalUnit-Display** en el contenedor de especificadores para mostrar. La cadena agregada al atributo **extraColumns** del objeto **organizationalUnit-Display** tendrá un aspecto parecido al siguiente.


```C++
canonicalName,Canonical Name,0,150,0
```



El **cuadro de diálogo** Agregar o quitar columnas muestra solo las columnas contenidas en el atributo **extraColumns** del objeto **displaySpecifier** del tipo de contenedor que se muestra. Si el **atributo extraColumns** no contiene ningún valor, el cuadro de diálogo Agregar **o** quitar columnas mostrará un conjunto fijo de columnas. Una copia del conjunto fijo de columnas se encuentra en el **atributo extraColumns** del **objeto default-Display.**

Para agregar una o varias columnas a la lista de columnas de un objeto específico, debe copiar todos los valores extraColumns del objeto **default-Display** al objeto de destino y, a continuación, agregar las columnas **personalizadas.** Si especifica el atributo **extraColumns** en una clase determinada, esa clase usará esas columnas y no las combinará con las columnas especificadas en la clase **default-Display.** Por lo tanto, otros cambios en **la clase default-Display** no tendrán ningún efecto en ese objeto.

Para mostrar una columna personalizada para todos los tipos de contenedor que no tienen ninguna columna personalizada registrada, agregue un valor para la columna al atributo **extraColumns** del objeto **default-Display.**

 

 




