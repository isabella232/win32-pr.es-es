---
title: Tres tipos de puntero
description: MIDL admite tres tipos de punteros para dar cabida a una amplia gama de aplicaciones.
ms.assetid: 6684c252-6fbe-49ca-9967-6d4baf5dc298
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9627c71b07c86ab2deb7e28bddcf6d30b1747cf7d44874620f4053383a5a948a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118923464"
---
# <a name="three-pointer-types"></a>Tres tipos de puntero

MIDL admite tres tipos de punteros para dar cabida a una amplia gama de aplicaciones. Los tres niveles diferentes se denominan punteros reference, unique y full, y se indican mediante los atributos ref , unique y **\[** [](/windows/desktop/Midl/ref) **\]** **\[** [](/windows/desktop/Midl/unique) **\]** **\[** [**ptr**](/windows/desktop/Midl/ptr) **\]** , respectivamente. Las clases de puntero descritas por estos atributos son mutuamente excluyentes. Los atributos de puntero se pueden aplicar a punteros en definiciones de tipo, tipos de valor devuelto de función, parámetros de función, miembros de estructuras o uniones, o elementos de matriz.

Los punteros incrustados son punteros que son miembros de estructuras o uniones. También pueden ser elementos de matrices. En la dirección , se supone que los **\[** [](/windows/desktop/Midl/in) **\]** punteros **\[ ref \]** incrustados apuntan al almacenamiento válido y no deben ser NULL. Esta situación es recursivamente aplicable a los punteros **\[ ref \]** a los que apuntan. En la **\[ dirección \]** , los punteros **\[ únicos \]** y completos incrustados (punteros con el **\[ atributo ptr) \]** pueden ser NULL o no.

Cualquier atributo de puntero colocado en un parámetro en la sintaxis de una declaración de función solo afecta al declarador de puntero situado más a la derecha para ese parámetro. Para afectar a otros declaradores de puntero, se deben usar tipos con nombre intermedios.

Las funciones que devuelven un puntero pueden tener un atributo de puntero como atributo de función. Los **\[ atributos unique \]** y **\[ ptr \]** deben aplicarse a los tipos devueltos de función. Las declaraciones de miembro que son punteros pueden especificar un atributo de puntero como atributo de campo. Un atributo de puntero también se puede aplicar como atributo de tipo en [**construcciones typedef.**](/windows/desktop/Midl/typedef)

Cuando no se especifica ningún atributo de puntero como un atributo de campo o tipo, los atributos de puntero se aplican según las reglas para una declaración de puntero sin atributos como se indica a continuación.

En el modo de compatibilidad con DCE, los atributos de puntero se determinan en el archivo IDL de definición. Si hay un atributo **\[** [**\_ predeterminado de**](/windows/desktop/Midl/pointer-default)puntero especificado en la interfaz de **\]** definición, se usa ese atributo. Si no **\[ hay ningún atributo \_ predeterminado \]** de puntero, todos los punteros sin atributos son punteros completos.

En el modo de extensiones de Microsoft, los atributos de puntero se pueden determinar importando archivos IDL y se aplican en el orden siguiente:

1.  Atributo de puntero explícito aplicado en el sitio de uso.
2.  Atributo **\[ ref, \]** cuando el puntero sin atributos es un parámetro de puntero de nivel superior.
3.  Atributo **\[ predeterminado \_ de \]** puntero especificado en la interfaz de definición.
4.  Atributo **\[ predeterminado \_ de \]** puntero especificado en la interfaz base.
5.  Atributo **único. \[ \]**

El atributo de interfaz predeterminado de puntero especifica los atributos de puntero predeterminados que se aplicarán a un declarador de puntero en una declaración de tipo, parámetro o tipo de valor devuelto cuando esa declaración no tenga aplicado un atributo de puntero **\[** [**\_**](/windows/desktop/Midl/pointer-default) **\]** explícito. El **\[ atributo \_ de \]** interfaz predeterminado del puntero no se aplica a un puntero de nivel superior sin atributos de un parámetro, que se supone que es **\[ ref \]**.

 

 