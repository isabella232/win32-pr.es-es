---
title: Crear un objeto en COM
description: Para usar una interfaz COM, el programa crea primero una instancia de un objeto que implementa esa interfaz.
ms.assetid: 75f2115d-d49d-4e4e-8f99-67a231559ba6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7e15874e1d4dcb6bc29fad90f40f90b478c805ccc7b0d0085f560a8b56e2247
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119913775"
---
# <a name="creating-an-object-in-com"></a>Crear un objeto en COM

Una vez que un subproceso ha inicializado la biblioteca COM, es seguro que el subproceso use interfaces COM. Para usar una interfaz COM, el programa crea primero una instancia de un objeto que implementa esa interfaz.

En general, hay dos maneras de crear un objeto COM:

-   El módulo que implementa el objeto podría proporcionar una función diseñada específicamente para crear instancias de ese objeto.
-   Como alternativa, COM proporciona una función de creación genérica denominada [**CoCreateInstance.**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)

Por ejemplo, tome el objeto `Shape` hipotético del tema [¿Qué es una interfaz COM?](what-is-a-com-interface-.md). En ese ejemplo, el `Shape` objeto implementa una interfaz denominada `IDrawable` . La biblioteca de gráficos que implementa el `Shape` objeto podría exportar una función con la firma siguiente.


```C++
// Not an actual Windows function. 

HRESULT CreateShape(IDrawable** ppShape);
```



Dada esta función, podría crear un nuevo `Shape` objeto como se muestra a continuación.


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



El *parámetro ppShape* es de tipo pointer-to-pointer-to- `IDrawable` . Si no ha visto este patrón antes, el direccionamiento indirecto doble podría ser desconcertante.

Tenga en cuenta los requisitos de la `CreateShape` función. La función debe devolver un `IDrawable` puntero al autor de la llamada. Pero el valor devuelto de la función ya se usa para el código de error o correcto. Por lo tanto, el puntero debe devolverse a través de un argumento a la función . El autor de la llamada pasará una variable de tipo a la función y la `IDrawable*` función sobrescribirá esta variable con un nuevo `IDrawable` puntero. En C++, solo hay dos maneras de que una función sobrescriba un valor de parámetro: pasar por referencia o pasar por dirección. COM usa el último paso por dirección. Y la dirección de un puntero es un puntero a un puntero, por lo que el tipo de parámetro debe ser `IDrawable**` .

Este es un diagrama para ayudar a visualizar lo que está ocurrindo.

![diagrama que muestra el direccionamiento indirecto de puntero doble](images/com03.png)

La `CreateShape` función usa la dirección de *pShape* ( `&pShape` ) para escribir un nuevo valor de puntero en *pShape*.

## <a name="cocreateinstance-a-generic-way-to-create-objects"></a>CoCreateInstance: una manera genérica de crear objetos

La [**función CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) proporciona un mecanismo genérico para crear objetos. Para comprender **CoCreateInstance,** tenga en cuenta que dos objetos COM pueden implementar la misma interfaz y un objeto puede implementar dos o más interfaces. Por lo tanto, una función genérica que crea objetos necesita dos fragmentos de información.

-   Objeto que se va a crear.
-   Interfaz que se va a obtener del objeto .

Pero, ¿cómo se indica esta información cuando se llama a la función? En COM, un objeto o una interfaz se identifica asignándolo un número de 128 bits, denominado identificador *único global* (GUID). Los GUID se generan de forma que sean únicos de forma eficaz. Los GUID son una solución al problema de cómo crear identificadores únicos sin una autoridad de registro central. A veces, los GUID se *denominan identificadores únicos universales* (UUD). Antes de COM, se usaban en DCE/RPC (Distributed Computing Environment/Remote Procedure Call). Existen varios algoritmos para crear nuevos GUID. No todos estos algoritmos garantizan estrictamente la unidad, pero la probabilidad de crear accidentalmente el mismo valor GUID dos veces es extremadamente pequeña, en efecto cero. Los GUID se pueden usar para identificar cualquier tipo de entidad, no solo objetos e interfaces. Sin embargo, este es el único uso que nos preocupa en este módulo.

Por ejemplo, la `Shapes` biblioteca podría declarar dos constantes GUID:


```C++
extern const GUID CLSID_Shape;
extern const GUID IID_IDrawable; 
```



(Puede suponer que los valores numéricos reales de 128 bits para estas constantes se definen en otra parte). La constante **CLSID \_ Shape** identifica el objeto , mientras que `Shape` la constante **IID \_ IDrawable** identifica la `IDrawable` interfaz. El prefijo "CLSID" significa identificador de *clase* y el *prefijo IID* significa identificador *de interfaz*. Se trata de convenciones de nomenclatura estándar en COM.

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



La [**función CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) tiene cinco parámetros. El primer y cuarto parámetro son el identificador de clase y el identificador de interfaz. De hecho, estos parámetros le dicen a la función "Crear el objeto Shape y damos un puntero a la interfaz IDrawable".

Establezca el segundo parámetro en **NULL.** (Para obtener más información sobre el significado de este parámetro, vea el tema [Agregación](/windows/desktop/com/aggregation) en la documentación com). El tercer parámetro toma un conjunto de marcas cuyo propósito principal es especificar el *contexto de ejecución* del objeto. El contexto de ejecución especifica si el objeto se ejecuta en el mismo proceso que la aplicación; en un proceso diferente en el mismo equipo; o en un equipo remoto. En la tabla siguiente se muestran los valores más comunes para este parámetro.



| Marca                       | Descripción                                                                                                                                                        |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CLSCTX \_ INPROC \_ SERVER** | Mismo proceso.                                                                                                                                                      |
| **CLSCTX \_ LOCAL \_ SERVER**  | Proceso diferente, mismo equipo.                                                                                                                                  |
| **CLSCTX \_ REMOTE \_ SERVER** | Equipo diferente.                                                                                                                                                |
| **CLSCTX \_ ALL**            | Use la opción más eficaz que admite el objeto . (La clasificación, de más eficaz a menos eficaz, es: en proceso, fuera de proceso y entre equipos). |



 

La documentación de un componente determinado podría decir qué contexto de ejecución admite el objeto. Si no es así, **use CLSCTX \_ ALL**. Si solicita un contexto de ejecución que el objeto no admite, la función [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) devuelve el código de error **REGDB \_ E \_ CLASSNOTREG**. Este código de error también puede indicar que clsid no corresponde a ningún componente registrado en el equipo del usuario.

El quinto parámetro de [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) recibe un puntero a la interfaz . Dado **que CoCreateInstance** es un mecanismo genérico, este parámetro no se puede escribir fuertemente. En su lugar, el tipo de datos **es void \* \*** y el autor de la llamada debe convertir la dirección del puntero en un tipo **void. \* \*** Ese es el propósito de la **conversión reinterpretación \_** en el ejemplo anterior.

Es fundamental comprobar el valor devuelto de [**CoCreateInstance.**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) Si la función devuelve un código de error, el puntero de interfaz COM no es válido e intentar desreferenciar puede provocar que el programa se bloquea.

Internamente, [**la función CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) usa varias técnicas para crear un objeto. En el caso más sencillo, busca el identificador de clase en el Registro. La entrada del Registro apunta a un archivo DLL o EXE que implementa el objeto . **CoCreateInstance** también puede usar información de un catálogo de COM+ o un manifiesto en paralelo (SxS). Independientemente de ello, los detalles son transparentes para el autor de la llamada. Para obtener más información sobre los detalles internos de **CoCreateInstance**, vea [Clientes y servidores COM](/windows/desktop/com/com-clients-and-servers).

El ejemplo que hemos estado usando es bastante derivado, por lo que ahora vamos a pasar a un ejemplo real de COM en acción: mostrar el cuadro de diálogo Abrir para que el usuario seleccione un `Shapes` archivo. 

## <a name="next"></a>Siguientes

[Ejemplo: El cuadro de diálogo Abrir](example--the-open-dialog-box.md)

 

 