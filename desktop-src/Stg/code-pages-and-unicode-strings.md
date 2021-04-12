---
title: Páginas de códigos y cadenas Unicode
description: Otro aspecto que se debe tener en cuenta al implementar IPropertySetStorage es el modo en que los nombres de propiedad Unicode se almacenan en el identificador de propiedad 0 (el Diccionario de nombres de propiedad), que no utiliza cadenas Unicode.
ms.assetid: 830c90c9-d2a5-4ecf-8cb6-9950ed5320bf
keywords:
- Páginas de códigos y cadenas Unicode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 508d508ec21e7e763a683e534cf485ebbeec018d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104356783"
---
# <a name="code-pages-and-unicode-strings"></a>Páginas de códigos y cadenas Unicode

Otro aspecto que se debe tener en cuenta al implementar [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) es el modo en que los nombres de propiedad Unicode se almacenan en el identificador de propiedad 0 (el Diccionario de nombres de propiedad), que no utiliza cadenas Unicode.

Unicode tiene oficialmente un valor de página de códigos de 1200. Para almacenar valores Unicode en el Diccionario de nombres de propiedad, use un valor de página de códigos de 1200 para todo el conjunto de propiedades (en el identificador de propiedad 1), especificado por la ausencia de la marca **\_ ANSI PROPSETFLAG** en [**IPropertySetStorage:: Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create). Tenga en cuenta que esto tiene el efecto secundario de almacenar todos los valores de cadena en el conjunto de propiedades en Unicode. En todas las páginas de códigos, el recuento que se encuentra al principio de un **VT \_ LPSTR** es un recuento de bytes, no un recuento de caracteres. Esto es necesario para proporcionar compatibilidad con clientes de versiones anteriores.

La implementación de archivo compuesto de [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) crea todos los conjuntos de propiedades nuevos completamente en Unicode (página de códigos 1200) o en la página de códigos ANSI del sistema actual. Esto se controla mediante la ausencia o la presencia de la marca **\_ ANSI PROPSETFLAG** en el parámetro *grfFlags* de [**IPropertySetStorage:: Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create).

Crear y abrir conjuntos de propiedades como Unicode. Para implementar esto, no establezca la marca **\_ ANSI PROPSETFLAG** en el parámetro *grfFlags* de [**IPropertySetStorage:: Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create). Evite usar valores de **VT \_ LPSTR** y, en su lugar, use los valores de **VT \_ LPWStr** . Cuando la página de códigos del conjunto de propiedades es Unicode, los valores de cadena de **VT \_ LPSTR** se convierten a Unicode cuando se almacenan y de nuevo a los valores de cadena multibyte cuando se recuperan.

Si se establece la marca **\_ ANSI PROPSETFLAG** como notificada a través de una llamada a [**IPropertyStorage:: Stat**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-stat) , se refleja si la página de códigos subyacente es o no es Unicode. Tenga en cuenta que el identificador de propiedad 1 se puede leer explícitamente para obtener información sobre la página de códigos.

Puede tener acceso al identificador de propiedad 1 a través de una llamada a [**IPropertyStorage:: ReadMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple). Sin embargo, es de solo lectura y no se puede actualizar con [**WriteMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writemultiple). Además, no se puede eliminar con [**DeleteMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-deletemultiple).

 

 




