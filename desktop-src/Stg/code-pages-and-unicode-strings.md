---
title: Páginas de códigos y cadenas Unicode
description: Otra consideración para implementar IPropertySetStorage es cómo se almacenan los nombres de propiedad Unicode en el identificador de propiedad 0 (el diccionario de nombres de propiedad), que no usa cadenas Unicode.
ms.assetid: 830c90c9-d2a5-4ecf-8cb6-9950ed5320bf
keywords:
- Páginas de códigos y cadenas Unicode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65a1d5a830d3d4e2fccbb61563e7a8a0447d74e7c427e5e2e0434e7194a2ad3e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119663605"
---
# <a name="code-pages-and-unicode-strings"></a>Páginas de códigos y cadenas Unicode

Otra consideración para implementar [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) es cómo se almacenan los nombres de propiedad Unicode en el identificador de propiedad 0 (el diccionario de nombres de propiedad), que no usa cadenas Unicode.

Unicode tiene oficialmente un valor de página de códigos de 1200. Para almacenar valores Unicode en el diccionario de nombres de propiedad, use un valor de página de códigos de 1200 para todo el conjunto de propiedades (en el identificador de propiedad 1), especificado por la ausencia de la marca **PROPSETFLAG \_ ANSI** en [**IPropertySetStorage::Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create). Tenga en cuenta que esto tiene el efecto secundario de almacenar todos los valores de cadena en la propiedad establecida en Unicode. En todas las páginas de códigos, el recuento que se encuentra al principio de **un \_ LPSTR de VT** es un recuento de bytes, no un recuento de caracteres. Esto es necesario para proporcionar compatibilidad con clientes de versión anterior.

La implementación de archivo compuesto de [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) crea todos los nuevos conjuntos de propiedades completamente en Unicode (página de códigos 1200) o en la página de códigos ANSI del sistema actual. Esto se controla mediante la ausencia o presencia de la marca **\_ PROPSETFLAG ANSI** en el *parámetro grfFlags* [**de IPropertySetStorage::Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create).

Cree y abra conjuntos de propiedades como Unicode. Para implementar esto, no establezca la marca **PROPSETFLAG \_ ANSI** en el parámetro *grfFlags* [**de IPropertySetStorage::Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create). Evite el uso **de valores \_ LPSTR de VT** y, en su lugar, use valores **\_ LPWSTR de VT.** Cuando la página de códigos del conjunto de propiedades es Unicode, los valores de cadena **\_ LPSTR** de VT se convierten en Unicode cuando se almacenan y de nuevo en valores de cadena multibyte cuando se recuperan.

Al establecer **la marca PROPSETFLAG \_ ANSI** como se indica a través de una llamada a [**IPropertyStorage::Stat,**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-stat) se refleja si la página de códigos subyacente es o no Unicode. Tenga en cuenta que el id. de propiedad 1 se puede leer explícitamente para obtener información sobre la página de códigos.

Puede acceder al identificador de propiedad 1 mediante una llamada a [**IPropertyStorage::ReadMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple). Sin embargo, es de solo lectura y es posible que no se actualice con [**WriteMultiple.**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writemultiple) Además, no se puede eliminar con [**DeleteMultiple.**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-deletemultiple)

 

 




