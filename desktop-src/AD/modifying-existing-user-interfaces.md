---
title: Modificación de las interfaces de usuario existentes
description: En el panel de resultados del complemento MMC de usuarios y equipos de Active Directory se muestran varias columnas de datos de atributos para los objetos de un contenedor, como los atributos name y Description.
ms.assetid: 55f4ae82-c380-42a9-beba-047ffd0131eb
ms.tgt_platform: multiple
keywords:
- Modificación de las interfaces de usuario existentes AD
- Complemento usuarios y equipos de AD, modificar pantalla
- Complemento usuarios y equipos de AD, Agregar columnas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd0765988a9ceed3e98966091ad94b868b96fd88
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903105"
---
# <a name="modifying-existing-user-interfaces"></a>Modificación de las interfaces de usuario existentes

En el panel de resultados del complemento MMC de usuarios y equipos de Active Directory se muestran varias columnas de datos de atributos para los objetos de un contenedor, como los atributos **Name** y **Description** . El complemento permite al usuario agregar y quitar las columnas que se muestran en el panel de resultados del complemento.

Para cambiar la pantalla, el usuario utiliza el menú desplegable **Ver** y selecciona **Agregar o quitar columnas**. En el cuadro de diálogo **Agregar o quitar columnas** , hay una lista de columnas que el usuario puede elegir para que se muestren en el panel de resultados.

El complemento MMC de Active Directory usuarios y equipos que se incluye con Windows Server 2003, Standard Edition, Windows Server 2003, Enterprise Edition y Windows Server 2003, Datacenter Edition, proporciona la capacidad de modificar la lista de columnas que se pueden mostrar en el panel de resultados del complemento de un contenedor. Esta característica solo existe si el complemento está destinado a un bosque con el esquema de Windows Server 2003.

Para agregar una columna a la lista, agregue un valor al atributo **Extracolumns** del especificador de presentación para el tipo de objeto al que está asociado el atributo. El atributo **Extracolumns** es un atributo de cadena de varios valores donde cada cadena tiene el formato siguiente.


```C++

<ldapdisplayname>,<column header>,<default visibility>,<width>,<unused>

```



En la tabla siguiente se muestra el contenido de estos valores.



| Value                        | Descripción                                                                                                                         |
|------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| " &lt; LDAPDisplayName &gt; "    | Contiene una cadena que representa el **LDAPDisplayName** del atributo.                                                         |
| " &lt; encabezado de columna &gt; "      | Contiene una cadena que representa el texto que se muestra en el encabezado de la columna.                                                  |
| " &lt; visibilidad predeterminada &gt; " | Contiene un valor numérico que es 0 si el atributo está oculto de forma predeterminada o 1 si el atributo es visible de forma predeterminada.               |
| " &lt; width &gt; "              | Contiene el ancho de la columna, en píxeles. Si este valor es-1, el ancho de la columna se establece en el ancho del encabezado de columna. |
| " &lt; sin usar &gt; "             | Sin usar. Debe ser cero.                                                                                                               |



 

Por ejemplo, para agregar una columna que mostrará el nombre canónico de los objetos en una unidad organizativa, se agrega un valor para el atributo **canonicalName** al atributo **extracolumns** del objeto **organizationalUnit-display** en el contenedor de especificadores de presentación. La cadena agregada al atributo **Extracolumns** del objeto **organizationalUnit-display** tendrá un aspecto similar al siguiente.


```C++
canonicalName,Canonical Name,0,150,0
```



En el cuadro de diálogo **Agregar o quitar columnas** solo se muestran las columnas contenidas en el atributo **extracolumns** del objeto **displaySpecifier** del tipo de contenedor que se está mostrando. Si el atributo **Extracolumns** no contiene ningún valor, el cuadro de diálogo **Agregar o quitar columnas** mostrará un conjunto fijo de columnas. En el atributo **Extracolumns** del objeto de **visualización predeterminado** se incluye una copia del conjunto fijo de columnas.

Para agregar una o más columnas a la lista de columnas de un objeto específico, debe copiar todos los valores de **Extracolumns** del objeto de **visualización predeterminado** en el objeto de destino y, a continuación, agregar las columnas personalizadas. Si especifica el atributo **Extracolumns** en una clase determinada, esa clase usará esas columnas y no las combinará con las columnas que se especifican en la clase **de presentación predeterminada** . Por lo tanto, los cambios adicionales en la clase **de presentación predeterminada** no surtirán efecto en ese objeto.

Para mostrar una columna personalizada para todos los tipos de contenedor que no tengan columnas personalizadas registradas, agregue un valor para la columna al atributo **Extracolumns** del objeto de **presentación predeterminada** .

 

 




