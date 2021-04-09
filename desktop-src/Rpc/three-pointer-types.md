---
title: Tres tipos de puntero
description: MIDL admite tres tipos de punteros para acomodar una amplia gama de aplicaciones.
ms.assetid: 6684c252-6fbe-49ca-9967-6d4baf5dc298
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efdcc9548568c8fca24d8abb40bf0eaa8b6e7da3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103995298"
---
# <a name="three-pointer-types"></a>Tres tipos de puntero

MIDL admite tres tipos de punteros para acomodar una amplia gama de aplicaciones. Los tres niveles distintos se denominan punteros de referencia, únicos y completos, y se indican mediante los atributos **\[** [**ref**](/windows/desktop/Midl/ref) **\]** , **\[** [**Unique**](/windows/desktop/Midl/unique) **\]** y **\[** [**ptr**](/windows/desktop/Midl/ptr) **\]** , respectivamente. Las clases de puntero descritas por estos atributos son mutuamente excluyentes. Los atributos de puntero se pueden aplicar a punteros en definiciones de tipo, tipos de valor devueltos de función, parámetros de función, miembros de estructuras o uniones, o elementos de matriz.

Los punteros incrustados son punteros que son miembros de estructuras o uniones. También pueden ser elementos de matrices. En la **\[** [](/windows/desktop/Midl/in) **\]** dirección, se supone que los punteros de **\[ referencia \]** incrustados apuntan al almacenamiento válido y no deben ser null. Esta situación se aplica de forma recursiva a todos los punteros de **\[ referencia \]** a los que apuntan. En la **\[ dirección \]** , los punteros **\[ únicos \]** y completos incrustados (punteros con el atributo **\[ ptr \]** ) pueden ser o no NULL.

Cualquier atributo de puntero colocado en un parámetro en la sintaxis de una declaración de función solo afecta al declarador de puntero situado más a la derecha para ese parámetro. Para que afecte a otros declaradores de puntero, se deben usar tipos con nombre intermedios.

Las funciones que devuelven un puntero pueden tener un atributo de puntero como atributo de función. Los atributos **\[ Unique \]** y **\[ ptr \]** se deben aplicar a los tipos de valor devuelto de función. Las declaraciones de miembros que son punteros pueden especificar un atributo de puntero como atributo de campo. Un atributo de puntero también se puede aplicar como atributo de tipo en las construcciones [**typedef**](/windows/desktop/Midl/typedef) .

Cuando no se especifica ningún atributo de puntero como atributo de campo o de tipo, los atributos de puntero se aplican según las reglas de una declaración de puntero sin atributos como se indica a continuación.

En el modo de compatibilidad con DCE, los atributos de puntero se determinan en el archivo IDL de definición. Si hay un atributo **\[** [**\_ predeterminado de puntero**](/windows/desktop/Midl/pointer-default) **\]** especificado en la interfaz de definición, se utiliza ese atributo. Si no hay ningún atributo **\[ \_ predeterminado \] de puntero** , todos los punteros sin atributos son punteros completos.

En el modo de extensiones de Microsoft, los atributos de puntero se pueden determinar mediante la importación de archivos IDL y se aplican en el orden siguiente:

1.  Atributo de puntero explícito aplicado en el sitio de uso.
2.  El atributo **\[ ref \]** , cuando el puntero sin atributos es un parámetro de puntero de nivel superior.
3.  Atributo **\[ \_ predeterminado \] de puntero** especificado en la interfaz de definición.
4.  Atributo **\[ \_ predeterminado \] de puntero** especificado en la interfaz base.
5.  Atributo **\[ único \]** .

El **\[** atributo de interfaz [**\_ predeterminado de puntero**](/windows/desktop/Midl/pointer-default) **\]** especifica los atributos de puntero predeterminados que se van a aplicar a un declarador de puntero en un tipo, parámetro o declaración de tipo de valor devuelto cuando esa declaración no tiene aplicado un atributo de puntero explícito. El atributo de interfaz **\[ \_ predeterminado \] del puntero** no se aplica a un puntero de nivel superior sin atributos de un parámetro, que se supone que es **\[ ref \]**.

 

 