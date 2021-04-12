---
title: Identificadores de propiedad reservados
description: Los identificadores de propiedad reservados no se pueden usar como identificadores de propiedad (ID). Se puede usar cualquier identificador de propiedad (ID), excepto 0, 1, y cualquier valor mayor o igual que 0x80000000. Estos valores de identificador de propiedad se reservan para que las usen las aplicaciones.
ms.assetid: d313a7b1-4cac-41f8-ba38-bf9cfaeb9d5c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a16a8e232a31864a402b01033a829183105905c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104487806"
---
# <a name="reserved-property-identifiers"></a>Identificadores de propiedad reservados

Los identificadores de propiedad reservados no se pueden usar como identificadores de propiedad (ID). Se puede usar cualquier identificador de propiedad (ID), excepto 0, 1, y cualquier valor mayor o igual que 0x80000000. Estos valores de identificador de propiedad se reservan para que las usen las aplicaciones.

En la tabla siguiente se enumeran los identificadores de propiedad reservados y la descripción de para la que está reservado el identificador de propiedad.



| IDENTIFICADOR de propiedad reservada | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0                    | Reservado para crear un [Diccionario de nombres para mostrar del conjunto de propiedades](property-set-display-name-dictionary.md)opcional. Esto permite a los usuarios del conjunto de propiedades adjuntar significado a las propiedades, más allá de las proporcionadas por el indicador de tipo.                                                                                                                                                                                                                                                                                                                                                                |
| 1                    | Se reserva como indicador de la página de códigos (Windows) o el script (Macintosh) que se va a usar al interpretar las cadenas en el conjunto de propiedades.<br/> Todos los valores de cadena del conjunto de propiedades deben almacenarse con la misma página de códigos. El valor del sistema operativo de origen en el encabezado del conjunto de propiedades (PROPERTYSETHEADER::d wOSVer) determina si el indicador de página de códigos corresponde a una página de códigos de Windows o a un script de Macintosh.<br/>                                                                                                                                                        |
| 0x80000000           | Reservado como indicación de la configuración regional para la que se escribe el conjunto de propiedades.<br/> La configuración regional predeterminada para un conjunto de propiedades es la configuración regional predeterminada del sistema (configuración \_ predeterminada del sistema local \_ ). Para obtener más información acerca de \_ la configuración regional predeterminada del sistema \_ , consulte las API de Win32. El valor predeterminado se utiliza en caso de que el indicador de configuración regional no exista en el conjunto de propiedades.<br/>                                                                                                                                                                                                                        |
| 0x80000003           | Reservado como indicador de los comportamientos del conjunto de propiedades. Este valor de identificador de propiedad es un UI4 de VT \_ y comienza con un tipo de datos **DWORD** que contiene el valor VT \_ UI4 seguido de un **DWORD** que indica el comportamiento del conjunto de propiedades.<br/> Actualmente, el único bit de este valor definido es el bit de orden inferior (0x1). Si se establece este bit, indica que los nombres de los conjuntos de propiedades, indicados por el identificador de propiedad 0, se deben considerar con distinción de mayúsculas y minúsculas. Si no se establece este bit o si la propiedad Behavior (ID 0x80000003) no existe, se debe considerar que los nombres no distinguen mayúsculas de minúsculas.<br/> |
| 0xFFFFFFFF           | Reservado para la comodidad de la programación. Nunca debe aparecer en un conjunto de propiedades serializado.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |



 

Los identificadores de propiedad con el conjunto de bits alto (es decir, los valores negativos) están reservados para su uso futuro por parte de Microsoft.

De las propiedades reservadas, aquellas con valores de identificador en el intervalo de 0x80000000 a 0xBFFFFFFF se consideran de solo lectura las implementaciones que no entienden su significado. Por ejemplo, si una implementación no entiende el significado de la propiedad 0x80000000, debe permitir que esa propiedad se lea pero no se escriba o elimine. Este tipo de implementación debe permitir la lectura, escritura o eliminación de una propiedad en el intervalo de 0xC0000000 a 0xFFFFFFFE. El ID. de propiedad 0xFFFFFFFF es un valor reservado y nunca debe aparecer en un conjunto de propiedades serializado.

## <a name="property-set-locale"></a>Configuración regional de conjunto de propiedades

Las aplicaciones pueden elegir entre admitir la configuración regional o usar el comportamiento predeterminado. Se recomienda que las aplicaciones permitan a los usuarios especificar una configuración regional operativa. Dichas aplicaciones deben escribir el identificador de configuración regional especificado por el usuario en la propiedad. Las aplicaciones que usan la configuración regional predeterminada de usuario ( \_ valor predeterminado del usuario de configuración regional \_ ) deben escribir el identificador de configuración regional predeterminado del usuario en la propiedad. Para obtener más información acerca de \_ la configuración predeterminada de usuario regional \_ , vea la API Win32.

> [!Note]  
> Si se usa la interfaz [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) para crear un conjunto de propiedades, la configuración regional predeterminada del usuario se escribe automáticamente como el indicador de configuración regional.

 

Las aplicaciones también deben controlar el caso de un objeto externo, que es aquél en el que la configuración regional no es la configuración regional de la aplicación, la configuración regional del usuario o la configuración regional del sistema.

La propiedad del indicador de configuración regional es de tipo VT \_ U14 y, por tanto, consta de un **valor DWORD** que contiene VT \_ U14, seguido de un **valor DWORD** que contiene el identificador de configuración regional (LCID), tal y como se define en la API Win32.

## <a name="code-page-indicator"></a>Indicador de página de códigos

Cuando una aplicación que no es el autor de un conjunto de propiedades cambia una propiedad de tipo cadena en el conjunto, debe examinar el indicador de página de códigos y realizar una de las siguientes acciones:

-   Escriba la cadena en el formato especificado por el indicador de página de códigos.
-   Reemplace y vuelva a escribir para cambiar la página de códigos.

Si una aplicación no puede reconocer este indicador, no debe modificar la propiedad. Todos los creadores de conjuntos de propiedades deben escribir un indicador de página de códigos. sin embargo, si el indicador de página de códigos no está presente, se debe suponer que es la página de códigos que prevalece en el equipo del lector.

> [!Note]  
> Si se utiliza la interfaz [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) para crear un conjunto de propiedades, el indicador de página de códigos se escribe automáticamente.

 

Los valores posibles de la página de códigos se proporcionan en la API de Win32 (para obtener más información, vea la función [**GetACP**](/windows/desktop/api/winnls/nf-winnls-getacp) ) y *en el volumen de Macintosh VI*, páginas 14-111. (Es posible que estos recursos no estén disponibles en algunos idiomas y países). Por ejemplo, la página de códigos ANSI se representa mediante 0x04E4 (1252 en formato decimal) mientras que la página de códigos de Unicode es 0x04B0 (1200 en formato decimal).

Se recomienda usar la página de códigos Unicode siempre que sea posible y usar VT \_ LPWStr en lugar de VT \_ LPSTR para evitar las conversiones de Unicode de multibyte <-> durante el almacenamiento y la recuperación. Usar la misma página de códigos para todos los conjuntos de propiedades es la única manera de lograr conjuntos de propiedades interoperables en todo el mundo. En la página de códigos Unicode o no Unicode, tenga en cuenta que el recuento al principio de un valor \_ BSTR de VT o VT \_ es un recuento de **bytes** y no un recuento de **caracteres** . Este recuento de bytes incluye uno o dos bytes cero al final de la cadena (el terminador **null** de la cadena).

El ID. de propiedad 1 es un \_ tipo I2 de VT y comienza con un valor **DWORD** que contiene el valor VT \_ I2 seguido de un **Short** que indica la página de códigos.

 

