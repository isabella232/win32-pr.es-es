---
title: Resolución de conflictos de nombres de función y propiedad en la automatización en extensiones
description: En este tema, \ 0034; objeto \ 0034; indica el objeto, como un todo, como un cliente ADSI lo ve. Es decir, ADSI y todas sus extensiones.
ms.assetid: 76207326-879e-408b-8004-06d940401a41
ms.tgt_platform: multiple
keywords:
- Resolución de conflictos de nombre de función y propiedad en la automatización en extensiones
- extensiones ADSI, resolver conflictos de nombre de función y propiedad en automatización
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9a7ac99b99ecdf0ee1b940f066d9e8166a15542
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104421406"
---
# <a name="resolution-of-functionproperty-name-conflicts-in-automation-in-extensions"></a>Resolución de conflictos de nombres de función y propiedad en la automatización en extensiones

En este tema, "objeto" indica el objeto, como un todo, como un cliente ADSI lo ve. Es decir, ADSI y todas sus extensiones.

## <a name="same-function-name-with-the-same-parameters"></a>El mismo nombre de función con los mismos parámetros

Si dos o más interfaces [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) duales de un objeto admiten una propiedad o un método con el mismo nombre, por ejemplo, **Func1**, la invocación se determina utilizando los siguientes criterios. Si el cliente tiene un puntero a una de las interfaces duales que admiten un método denominado **Func1** y si el entorno de automatización admite el acceso vtable, **Func1** se invoca directamente a través del acceso vtable de ADSI.

Si alguna de las condiciones anteriores es falsa, se llama a [**IDispatch:: GetIDsOfNames**](/windows/win32/api/oaidl/nf-oaidl-idispatch-getidsofnames) y [**IDispatch:: Invoke**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke) para invocar **Func1**.

Para obtener más información y una breve explicación sobre cómo un cliente puede Agregar un puntero a una interfaz dual y una descripción de los tipos de entornos que admiten el acceso vtable, vea [enlace en tiempo de ejecución frente al acceso vtable en el modelo de extensión ADSI](late-binding-vs--vtable-access-in-the-adsi-extension-model.md).

Dado que todos los objetos de extensión redirigen las funciones [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) al agregador, el agregador controla qué **Func1** se invoca. Las reglas son:

-   Si alguna interfaz y solo habrá una, si la hubiera, en el agregador (ADSI) es compatible con una función denominada **FUNC1**, el agregador invoca su propio **Func1**.
-   De lo contrario, el agregador recorre cada una de sus extensiones, en el orden enumerado en el registro, y busca la primera extensión que implementa una función denominada **Func1**. Es posible, pero improbable, que varias interfaces [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) duales en esta primera extensión tengan una función denominada **Func1**. La extensión debe determinar qué **Func1** siempre se debe invocar en Automation.

## <a name="same-function-name-with-different-parameters"></a>El mismo nombre de función con parámetros diferentes

En la sección anterior se describe cómo resolver conflictos de nombres de función, es decir, nombres de función que tienen el mismo nombre de función y la misma lista de parámetros, como número, tipo y orden, cuando se produce en la automatización. ¿Qué ocurre si dos funciones tienen el mismo nombre pero parámetros diferentes? Si un cliente ADSI invoca la función mediante [**IDispatch:: GetIDsOfNames**](/windows/win32/api/oaidl/nf-oaidl-idispatch-getidsofnames) sin usar varios nombres para especificar los parámetros, el modelo de extensión ADSI no puede eliminar la ambigüedad de las funciones. Según el esquema de resolución descrito anteriormente, la primera extensión del registro que admite esta función a través de una de sus interfaces tiene su versión de esta función invocada, y la llamada puede producir un error o producir resultados incorrectos.

Por ejemplo:

-   Extn1 (en primer lugar, en el registro en la clase CA, mayor prioridad) admite **IInterface1**.
-   Extn2 (tercer en el registro bajo la clase CA – Lower Priority) admite **IInterface2**.
-   **IInterface1** admite **method1 (int parámetro1, int parám2)**.
-   **IInterface2** admite **method1 (int parám1)**.

Un cliente ADSI tiene un puntero de interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) a un objeto de clase CA. Quiere invocar **IInterface2:: method1**. Si el cliente llama a "pDispatch->GetIDsOfNames (IID \_ null, rgszNames, 1, \_ mi LCID, rgDispId)" simplemente almacenando el nombre de función "method1" en *rgszNames \[ 0 \]*, entonces **IInterface1:: method1** en lugar del valor deseado **IInterface2:: method1** se invoca y la función produce un error porque el número de parámetros es diferente.

Para minimizar este problema, los desarrolladores de extensiones pueden prefijar sus nombres de función con sus propios identificadores específicos y evitar diseños de interfaz que usen funciones del mismo nombre, pero parámetros diferentes.

Si se produce un conflicto de nombres, los clientes ADSI pueden evitar el problema mediante el acceso vtable directo si la interfaz es una interfaz dual. Si el acceso de vtable directo no es posible, los clientes ADSI deben llamar a [**IDispatch:: GetIDsOfNames**](/windows/win32/api/oaidl/nf-oaidl-idispatch-getidsofnames) con varios nombres, especificando los nombres de función, así como los parámetros de la matriz *rgszNames* descrita anteriormente.

Visual Basic 5 no llama a la función [**IDispatch:: GetIDsOfNames**](/windows/win32/api/oaidl/nf-oaidl-idispatch-getidsofnames) con varios nombres. Es decir, solo pasa el nombre de la función a **GetIDsOfNames**, pero no los argumentos. Sin embargo, Visual Basic 5 permite a los usuarios invocar una función mediante el acceso vtable directo, en lugar de invocar la función **IDispatch:: GetIDsOfNames** si la interfaz es una interfaz dual. Los desarrolladores deben usar el acceso vtable directo, si es posible.

Para obtener más información acerca de la resolución de conflictos de nombres, vea el [ejemplo para resolver conflictos de nombres de función](example-for-resolving-function-name-conflicts.md).

 

 