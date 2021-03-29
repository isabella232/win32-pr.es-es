---
title: Acerca del esquema de Active Directory
description: Cada objeto de Active Directory Domain Services es una instancia de una clase de objeto definida en el esquema de Active Directory.
ms.assetid: 8fc9cd2d-8fed-4fda-918c-79b01f9a19bb
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f55513b359a7ef293b005d93a20ac43f470d515
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903005"
---
# <a name="about-the-active-directory-schema"></a>Acerca del esquema de Active Directory

Cada objeto de Active Directory Domain Services es una instancia de una clase de objeto definida en el esquema de Active Directory. Una clase de objeto representa una categoría de objetos, como usuarios, impresoras o aplicaciones, que comparten un conjunto de características comunes. La definición de cada clase de objeto contiene una lista de los atributos que se pueden usar para describir instancias de la clase. Por ejemplo, la clase User tiene atributos como **givenName**, **surname** y **streetAddress**. La lista de atributos de una clase se divide en las que un objeto de esa clase debe contener y los atributos adicionales que puede contener un objeto. El directorio se organiza en una jerarquía; en la definición de cada clase se enumeran también las clases cuyos objetos pueden ser elementos primarios de los objetos de una clase determinada, lo que controla la forma de la jerarquía de directorios.

El esquema también define formalmente cada atributo. La definición de cada atributo incluye los identificadores únicos del atributo, la sintaxis del atributo (es decir, el tipo de datos para los valores del atributo), los límites de intervalo opcionales para los valores de atributo, si el atributo solo puede tener un valor o varios valores, y si el atributo está indizado. El esquema de directorio define cada atributo exactamente una vez: las definiciones de clase de objeto contienen referencias a los atributos definidos en el esquema. Por ejemplo, el atributo "Description" solo se define una vez y varias clases de objeto hacen referencia a él. Esto es diferente de un esquema de base de datos relacional, donde los "atributos" (columnas) se definen por separado para cada tabla.

 

 




