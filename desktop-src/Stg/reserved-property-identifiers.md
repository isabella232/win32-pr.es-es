---
title: Identificadores de propiedad reservada
description: Los identificadores de propiedad reservada no se pueden usar como identificadores de propiedad (ID). Cualquier identificador de propiedad (ID) se puede usar excepto 0, 1 y cualquier valor mayor o igual que 0x80000000. Estos valores de identificador de propiedad están reservados para que los usen las aplicaciones.
ms.assetid: d313a7b1-4cac-41f8-ba38-bf9cfaeb9d5c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05053fd2a31a5e8ceec63420e74884484abef12d44dcfe3e7023c81b5e67e27a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119683065"
---
# <a name="reserved-property-identifiers"></a>Identificadores de propiedad reservada

Los identificadores de propiedad reservada no se pueden usar como identificadores de propiedad (ID). Cualquier identificador de propiedad (ID) se puede usar excepto 0, 1 y cualquier valor mayor o igual que 0x80000000. Estos valores de identificador de propiedad están reservados para que los usen las aplicaciones.

En la tabla siguiente se enumeran los identificadores de propiedad reservados y la descripción de para qué se reserva el identificador de propiedad.



| Identificador de propiedad reservada | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0                    | Reservado para crear un diccionario [de nombres para mostrar del conjunto de propiedades opcional.](property-set-display-name-dictionary.md) Esto permite a los usuarios del conjunto de propiedades asociar significado a las propiedades, más allá de las proporcionadas por el indicador de tipo.                                                                                                                                                                                                                                                                                                                                                                |
| 1                    | Reservado como indicador de la página de códigos (Windows) o Script (Macintosh) que se usará al interpretar las cadenas del conjunto de propiedades.<br/> Todos los valores de cadena del conjunto de propiedades deben almacenarse con la misma página de códigos. El valor del sistema operativo de origen en el encabezado del conjunto de propiedades (PROPERTYSETHEADER::d wOSVer) determina si el indicador de página de códigos corresponde a una página de códigos Windows o un script macintosh.<br/>                                                                                                                                                        |
| 0x80000000           | Reservado como indicación de la configuración regional para la que se escribe el conjunto de propiedades.<br/> La configuración regional predeterminada para un conjunto de propiedades es la configuración regional predeterminada del sistema (LOCALE \_ SYSTEM \_ DEFAULT). Para obtener más información sobre LOCALE \_ SYSTEM \_ DEFAULT, consulte las API de Win32. El valor predeterminado se usa en caso de que el indicador de configuración regional no exista en el conjunto de propiedades.<br/>                                                                                                                                                                                                                        |
| 0x80000003           | Reservado como indicador de los comportamientos del conjunto de propiedades. Este valor de identificador de propiedad es VT UI4 y comienza con un tipo de datos DWORD que contiene el valor VT UI4 seguido de \_ un  \_ **DWORD** que indica el comportamiento del conjunto de propiedades.<br/> Actualmente, el único bit de este valor que se define es el bit de orden bajo (0x1). Si se establece este bit, indica que los nombres de conjunto de propiedades, indicados por el identificador de propiedad 0, se deben considerar con distinguen mayúsculas de minúsculas. Si no se establece este bit o si la propiedad de comportamiento (id. 0x80000003) no existe, los nombres deben considerarse no diferenciadores entre mayúsculas y minúsculas.<br/> |
| 0xFFFFFFFF           | Reservado para la comodidad de la programación. Nunca debería aparecer en un conjunto de propiedades serializadas.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |



 

Los identificadores de propiedad con el conjunto de bits alto (es decir, valores negativos) están reservados para su uso futuro por parte de Microsoft.

De las propiedades reservadas, aquellas con valores de identificador en el intervalo 0x80000000 a 0xBFFFFFFF se consideran de solo lectura por implementaciones que no comprenden su significado. Por ejemplo, si una implementación no entiende el significado de la propiedad 0x80000000, debe permitir que esa propiedad se lea, pero no se escriba ni elimine. Esta implementación debe permitir que una propiedad del intervalo 0xC0000000 se 0xFFFFFFFE leer, escribir o eliminar. El identificador de 0xFFFFFFFF es un valor reservado y nunca debe aparecer en un conjunto de propiedades serializado.

## <a name="property-set-locale"></a>Configuración regional del conjunto de propiedades

Las aplicaciones pueden optar por admitir la configuración regional o usar el comportamiento predeterminado. Se recomienda que las aplicaciones permitan a los usuarios especificar una configuración regional en funcionamiento. Estas aplicaciones deben escribir el identificador de configuración regional especificado por el usuario en la propiedad . Las aplicaciones que usan la configuración regional predeterminada del usuario (LOCALE USER DEFAULT) deben escribir el identificador de configuración regional predeterminado del usuario \_ \_ en la propiedad . Para obtener más información sobre LOCALE \_ USER \_ DEFAULT, consulte la API de Win32.

> [!Note]  
> Si la [**interfaz IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) se usa para crear un conjunto de propiedades, la configuración regional predeterminada del usuario se escribe automáticamente como indicador de configuración regional.

 

Las aplicaciones también deben controlar el caso de un objeto externo, que es donde la configuración regional no es la configuración regional de la aplicación, la configuración regional del usuario o la configuración regional del sistema.

La propiedad del indicador de configuración regional es de tipo VT U14 y, por tanto, consta de un DWORD que contiene VT U14, seguido de un DWORD que contiene el identificador de configuración regional (LCID), tal como se define en la \_ API  \_ win32. 

## <a name="code-page-indicator"></a>Indicador de página de códigos

Cuando una aplicación que no es el autor de un conjunto de propiedades cambia una propiedad de tipo cadena en el conjunto, debe examinar el indicador de página de códigos y realizar una de las siguientes acciones:

-   Escriba la cadena en el formato especificado por el indicador de página de códigos.
-   Reemplace y vuelva a escribir para cambiar la página de códigos.

Si una aplicación no puede reconocer este indicador, no debe modificar la propiedad . Todos los creadores de conjuntos de propiedades deben escribir un indicador de página de códigos; sin embargo, si el indicador de página de códigos no está presente, se debe asumir la página de códigos correspondiente en el equipo del lector.

> [!Note]  
> Si se [**usa la interfaz IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) para crear un conjunto de propiedades, el indicador de página de códigos se escribe automáticamente.

 

Los valores posibles de la página de códigos se dan en la API de Win32 (para obtener más información, vea la función [**GetACP)**](/windows/desktop/api/winnls/nf-winnls-getacp) y dentro del volumen VI de *Macintosh,* páginas 14-111. (Es posible que estos recursos no estén disponibles en algunos idiomas y países). Por ejemplo, la página de códigos ANSI de EE. UU. se representa mediante 0x04E4 (1252 en decimal) mientras que la página de códigos para Unicode es 0x04B0 (1200 en decimal).

Se recomienda usar la página de códigos Unicode siempre que sea posible y usar VT LPWSTR en lugar de VT LPSTR para evitar conversiones Unicode \_ <-> multibyte durante el almacenamiento y la \_ recuperación. El uso de la misma página de códigos para todos los conjuntos de propiedades es la única manera de lograr conjuntos de propiedades interoperables en todo el mundo. En la página de códigos Unicode o no Unicode, tenga en cuenta que el recuento al principio de una VT LPSTR o VT BSTR es un recuento de bytes y no un \_ \_ recuento **de** caracteres.  Este recuento de bytes incluye uno o dos bytes cero al final de la cadena (terminador **NULL** de la cadena).

Id. de propiedad 1 es un tipo VT I2 y comienza con un DWORD que contiene el valor VT I2 seguido de un short que \_ indica la página de  \_ códigos. 

 

