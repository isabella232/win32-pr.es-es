---
title: Resolución de conflictos de nombre de función o propiedad en Automation en extensiones
description: En este tema, \ 0034;object \ 0034; indica el objeto, como un todo, como un cliente ADSI lo ve. Es decir, ADSI y todas sus extensiones.
ms.assetid: 76207326-879e-408b-8004-06d940401a41
ms.tgt_platform: multiple
keywords:
- Resolución de conflictos de nombre de función y propiedad en Automation en extensiones
- ADSI de extensiones, resolución de conflictos de nombre de propiedad y función en Automation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53701c95672fe209cb57a15e3292e1269dc37e66e36f041110dd502f8a8a1486
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119637545"
---
# <a name="resolution-of-functionproperty-name-conflicts-in-automation-in-extensions"></a>Resolución de conflictos de nombre de función o propiedad en Automation en extensiones

En este tema, "object" indica el objeto en su conjunto, ya que un cliente ADSI lo ve. Es decir, ADSI y todas sus extensiones.

## <a name="same-function-name-with-the-same-parameters"></a>Mismo nombre de función con los mismos parámetros

Si dos o más interfaces [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) duales de un objeto admiten una propiedad o un método del mismo nombre, por ejemplo, **Func1,** la invocación se determina con los criterios siguientes. Si el cliente tiene un puntero a una de las interfaces duales que admiten un método denominado **Func1** y si el entorno de Automation admite el acceso vtable, **Func1** se invoca directamente a través del acceso adsi vtable.

Si cualquiera de las condiciones anteriores es false, se llama a [**IDispatch::GetIDsOfNames**](/windows/win32/api/oaidl/nf-oaidl-idispatch-getidsofnames) e [**IDispatch::Invoke**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke) para invocar **Func1.**

Para obtener más información y una breve explicación sobre cómo un cliente puede agregar un puntero a una interfaz dual y una descripción de los tipos de entornos que admiten el acceso vtable, vea Enlace en tiempo de ejecución frente al acceso de Vtable en el modelo de [extensión ADSI](late-binding-vs--vtable-access-in-the-adsi-extension-model.md).

Dado que todos los objetos de extensión redirigen las funciones [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) de nuevo al agregador, el agregador controla qué **func1** se invoca. Las reglas son:

-   Si alguna interfaz, y solo habrá una, si existe, en el agregador (ADSI) admite una función denominada **Func1**, el agregador invoca su propio **Func1**.
-   De lo contrario, el agregador pasa por cada una de sus extensiones, en el orden indicado en el registro, y busca la primera extensión que implementa una función denominada **Func1**. Es posible, pero improbable, que varias interfaces [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) duales de esta primera extensión tengan una función denominada **Func1**. La extensión debe determinar qué **Func1** debe invocarse siempre en Automation.

## <a name="same-function-name-with-different-parameters"></a>Mismo nombre de función con parámetros diferentes

En la sección anterior se describe cómo resolver conflictos de nombres de función, es decir, nombres de función que tienen el mismo nombre de función y la misma lista de parámetros, como número, tipo y orden, cuando se produce en Automation. ¿Qué ocurre si dos funciones tienen el mismo nombre pero parámetros diferentes? Si un cliente ADSI invoca la función mediante [**IDispatch::GetIDsOfNames**](/windows/win32/api/oaidl/nf-oaidl-idispatch-getidsofnames) sin usar varios nombres para especificar los parámetros, el modelo de extensión ADSI no puede eliminar la ambigüedad de las funciones. En función del esquema de resolución descrito anteriormente, la primera extensión del Registro que admite esta función a través de una de sus interfaces tiene su versión de esta función invocada y la llamada puede producir errores o producir resultados incorrectos.

Por ejemplo:

-   Extn1 (primero en el registro en la clase CA : prioridad más alta) admite **IInterface1.**
-   Extn2 (tercero en el registro en la clase CA : prioridad inferior) admite **IInterface2.**
-   **IInterface1 admite** **Method1(int param1, int param2)**.
-   **IInterface2 admite** **Method1(int param1)**.

Un cliente ADSI tiene un [**puntero de interfaz IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) a un objeto de la clase CA. Quiere invocar **IInterface2::Method1**. Si el cliente llama a "pDispatch->GetIDsOfNames(IID \_ NULL, rgszNames, 1, MY LCID, rgDispId)" simplemente almacenando el nombre de función \_ "Method1" en *rgszNames \[ 0, \]* se invoca **IInterface1::Method1** en lugar de la **IInterface2::Method1** deseada y se produce un error en la función porque el número de parámetros es diferente.

Para minimizar este problema, los desarrolladores de extensiones pueden antefirer sus nombres de función con sus propios identificadores específicos y evitar los diseños de interfaz que usan funciones del mismo nombre, pero parámetros diferentes.

Si se produce un conflicto de nombres, los clientes ADSI pueden evitar el problema mediante el acceso directo a vtable si la interfaz es una interfaz dual. Si no es posible el acceso directo a la tabla virtual, los clientes ADSI deben llamar a [**IDispatch::GetIDsOfNames**](/windows/win32/api/oaidl/nf-oaidl-idispatch-getidsofnames) con varios nombres, especificando los nombres de función, así como los parámetros de la *matriz rgszNames descrita* anteriormente.

Visual Basic 5 no llama a la función [**IDispatch::GetIDsOfNames**](/windows/win32/api/oaidl/nf-oaidl-idispatch-getidsofnames) con varios nombres. Es decir, solo pasa el nombre de la función a **GetIDsOfNames,** pero no argumentos. Sin embargo, Visual Basic 5 permite a los usuarios invocar una función mediante el acceso directo a vtable, en lugar de invocar la función **IDispatch::GetIDsOfNames** si la interfaz es una interfaz dual. Los desarrolladores deben usar el acceso directo a vtable, si es posible.

Para obtener más información sobre la resolución de conflictos de nombres, vea [Ejemplo para resolver conflictos de nombres de función.](example-for-resolving-function-name-conflicts.md)

 

 