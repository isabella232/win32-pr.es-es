---
title: Crear un objeto en COM
description: Para usar una interfaz COM, el programa crea primero una instancia de un objeto que implementa esa interfaz.
ms.assetid: 75f2115d-d49d-4e4e-8f99-67a231559ba6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96f96e4d9c2afbac028bfcefffcec6a070c78c8b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104420624"
---
# <a name="creating-an-object-in-com"></a>Crear un objeto en COM

Una vez que un subproceso ha inicializado la biblioteca COM, es seguro que el subproceso use las interfaces COM. Para usar una interfaz COM, el programa crea primero una instancia de un objeto que implementa esa interfaz.

En general, hay dos maneras de crear un objeto COM:

-   El módulo que implementa el objeto podría proporcionar una función diseñada específicamente para crear instancias de ese objeto.
-   Como alternativa, COM proporciona una función de creación genérica denominada [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).

Por ejemplo, tome el `Shape` objeto hipotético del tema [¿Qué es una interfaz com?](what-is-a-com-interface-.md). En ese ejemplo, el `Shape` objeto implementa una interfaz denominada `IDrawable` . La biblioteca de gráficos que implementa el `Shape` objeto podría exportar una función con la siguiente firma.


```C++
// Not an actual Windows function. 

HRESULT CreateShape(IDrawable** ppShape);
```



Dada esta función, podría crear un nuevo `Shape` objeto como se indica a continuación.


```C++
IDrawable *pShape;

HRESULT hr = CreateShape(&pShape);
if (SUCCEEDED(hr))
{
    // Use the Shape object.
}
else
{
    // An error occurred.
}
```



El parámetro *ppShape* es de tipo puntero a puntero a `IDrawable` . Si no ha encontrado este patrón antes, el direccionamiento indirecto doble podría ser desconcertantes.

Tenga en cuenta los requisitos de la `CreateShape` función. La función debe devolver un `IDrawable` puntero al llamador. Pero el valor devuelto de la función ya se usa para el código de error o de operación correcta. Por lo tanto, el puntero se debe devolver a través de un argumento a la función. El autor de la llamada pasará una variable de tipo `IDrawable*` a la función y la función sobrescribirá esta variable con un nuevo `IDrawable` puntero. En C++, solo hay dos maneras de que una función sobrescriba un valor de parámetro: pasar por referencia o pasar por dirección. COM utiliza el último, pass-by-Address. Y la dirección de un puntero es un puntero a un puntero, por lo que el tipo de parámetro debe ser `IDrawable**` .

Este es un diagrama que le ayudará a visualizar lo que está ocurriendo.

![diagrama que muestra el direccionamiento indirecto de puntero doble](images/com03.png)

La `CreateShape` función usa la dirección de *pShape* ( `&pShape` ) para escribir un nuevo valor de puntero en *pShape*.

## <a name="cocreateinstance-a-generic-way-to-create-objects"></a>CoCreateInstance: una manera genérica de crear objetos

La función [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) proporciona un mecanismo genérico para crear objetos. Para comprender **CoCreateInstance**, tenga en cuenta que dos objetos com pueden implementar la misma interfaz y un objeto puede implementar dos o más interfaces. Por lo tanto, una función genérica que crea objetos necesita dos fragmentos de información.

-   Objeto que se va a crear.
-   La interfaz que se va a obtener del objeto.

Pero, ¿cómo se indica esta información cuando se llama a la función? En COM, un objeto o una interfaz se identifica asignando un número de 128 bits, denominado *identificador único global* (GUID). Los GUID se generan de forma que sean realmente únicos. Los GUID son una solución para el problema de cómo crear identificadores únicos sin una entidad de registro central. Los GUID a veces se denominan *identificadores únicos universales* (UUID). Antes de COM, se usaban en DCE/RPC (entorno informático distribuido o llamada a procedimiento remoto). Existen varios algoritmos para crear nuevos GUID. No todos estos algoritmos garantizan estrictamente la unicidad, pero la probabilidad de crear accidentalmente el mismo valor GUID dos veces es extremadamente pequeña, pero es realmente cero. Los GUID se pueden usar para identificar cualquier tipo de entidad, no solo objetos e interfaces. Sin embargo, este es el único uso que nos preocupa en este módulo.

Por ejemplo, la `Shapes` biblioteca podría declarar dos constantes GUID:


```C++
extern const GUID CLSID_Shape;
extern const GUID IID_IDrawable; 
```



(Puede suponer que los valores numéricos reales de 128 bits para estas constantes se definen en otro lugar). La **\_ forma de CLSID** constante identifica el `Shape` objeto, mientras que el **IID constante \_ IDrawable** identifica la `IDrawable` interfaz. El prefijo "CLSID" representa el *identificador de clase* y el *IID* de prefijo representa el identificador de *interfaz*. Se trata de convenciones de nomenclatura estándar en COM.

Dados estos valores, crearía una nueva `Shape` instancia de la siguiente manera:


```C++
IDrawable *pShape;
hr = CoCreateInstance(CLSID_Shape, NULL, CLSCTX_INPROC_SERVER, IID_Drawable,
     reinterpret_cast<void**>(&pShape));

if (SUCCEEDED(hr))
{
    // Use the Shape object.
}
else
{
    // An error occurred.
}
```



La función [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) tiene cinco parámetros. Los parámetros primero y cuarto son el identificador de clase y el identificador de interfaz. En efecto, estos parámetros indican a la función "cree el objeto de forma y proporcione un puntero a la interfaz IDrawable".

Establezca el segundo parámetro en **null**. (Para obtener más información sobre el significado de este parámetro, vea la [agregación](/windows/desktop/com/aggregation) de temas en la documentación de com). El tercer parámetro toma un conjunto de marcas cuyo propósito principal es especificar el *contexto de ejecución* para el objeto. El contexto de ejecución especifica si el objeto se ejecuta en el mismo proceso que la aplicación; en un proceso diferente en el mismo equipo; o en un equipo remoto. En la tabla siguiente se muestran los valores más comunes para este parámetro.



| Marca                       | Descripción                                                                                                                                                        |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_servidor INproc de CLSCTX \_** | Mismo proceso.                                                                                                                                                      |
| **\_servidor local de CLSCTX \_**  | Proceso diferente, el mismo equipo.                                                                                                                                  |
| **\_servidor remoto \_ CLSCTX** | Equipo diferente.                                                                                                                                                |
| **CLSCTX \_ todo**            | Use la opción más eficaz que admite el objeto. (La clasificación, de más eficaz a menos eficiente, es: en proceso, fuera de proceso y entre equipos). |



 

La documentación de un componente determinado puede indicarle el contexto de ejecución que admite el objeto. Si no es así, use **CLSCTX \_ All**. Si solicita un contexto de ejecución que no admite el objeto, la función [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) devuelve el código de error **REGDB \_ E \_ CLASSNOTREG**. Este código de error también puede indicar que el CLSID no corresponde a ningún componente registrado en el equipo del usuario.

El quinto parámetro de [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) recibe un puntero a la interfaz. Dado que **CoCreateInstance** es un mecanismo genérico, este parámetro no se puede escribir fuertemente tipado. En su lugar, el tipo de datos es **void \* \*** y el llamador debe forzar la dirección del puntero a un **tipo \* \* void** . Este es el propósito de la **\_ conversión de reinterpretación** en el ejemplo anterior.

Es fundamental comprobar el valor devuelto de [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance). Si la función devuelve un código de error, el puntero de interfaz COM no es válido y, al intentar desreferenciarlo, puede provocar que el programa se bloquee.

Internamente, la función [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) utiliza varias técnicas para crear un objeto. En el caso más simple, busca el identificador de clase en el registro. La entrada del registro señala a un archivo DLL o EXE que implementa el objeto. **CoCreateInstance** también puede usar información de un catálogo com+ o un manifiesto en paralelo (SxS). Independientemente de, los detalles son transparentes para el autor de la llamada. Para obtener más información acerca de los detalles internos de **CoCreateInstance**, consulte [com clients and Servers](/windows/desktop/com/com-clients-and-servers).

El `Shapes` ejemplo que hemos usado es algo inventado, por lo que ahora vamos a pasar a un ejemplo real de com en acción: mostrar el cuadro de diálogo **abrir** para que el usuario seleccione un archivo.

## <a name="next"></a>Siguientes

[Ejemplo: el cuadro de diálogo abrir](example--the-open-dialog-box.md)

 

 