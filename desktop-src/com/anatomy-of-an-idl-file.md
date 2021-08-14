---
title: Anatomía de un archivo IDL
description: Estos archivos IDL de ejemplo muestran las construcciones fundamentales de la definición de interfaz.
ms.assetid: 9c276b8a-5342-4c09-91a7-c9a9f0f83c73
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 531d46bfcfa0ef4e4eee075ae65b64dd0c80a8f6a51543a1762a0ddcd8a03888
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118311339"
---
# <a name="anatomy-of-an-idl-file"></a>Anatomía de un archivo IDL

Estos archivos IDL de ejemplo muestran las construcciones fundamentales de la definición de interfaz. La asignación de memoria, la serialización personalizada y la mensajería asincrónica son solo algunas de las características que puede implementar en una interfaz COM personalizada. Los atributos MIDL se usan para definir interfaces COM. Para obtener más información sobre la implementación de interfaces y bibliotecas de tipos, incluido un resumen de los atributos MIDL, vea Definiciones de interfaz y [bibliotecas](/windows/desktop/Midl/interface-definitions-and-type-libraries) de tipos en la Guía y referencia del programador de MIDL. Para obtener una referencia completa de todos los atributos, palabras clave y directivas de MIDL, vea midl language reference (Referencia [del lenguaje MIDL).](/windows/desktop/Midl/midl-language-reference)

## <a name="exampleidl"></a>Example.idl

El siguiente archivo IDL de ejemplo define dos interfaces COM. A partir de este archivo IDL, Midl.exe código proxy/stub y serialización de código y archivos de encabezado. Una dissección línea a línea sigue el ejemplo.

``` syntax
//
// Example.idl 
//
import "mydefs.h","unknwn.idl"; 
[
object,
uuid(a03d1420-b1ec-11d0-8c3a-00c04fc31d2f),
] interface IFace1 : IUnknown
{
HRESULT MethodA([in] short Bread, [out] BKFST * pBToast);
HRESULT MethodB([in, out] BKFST * pBPoptart);
};
 
[
object,
uuid(a03d1421-b1ec-11d0-8c3a-00c04fc31d2f),
pointer_default(unique)
] interface IFace2 : IUnknown
{
HRESULT MethodC([in] long Max,
                [in, max_is(Max)] BkfstStuff[ ],
                [out] long * pSize,
                [out, size_is( , *pSize)] BKFST ** ppBKFST);
}; 
 
```

La instrucción de importación de [**IDL**](/windows/desktop/Midl/import) se usa aquí para traer un archivo de encabezado, Mydefs.h, que contiene tipos definidos por el usuario, y Unknwn.idl, que contiene la definición de [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown), de la que derivan IFace1 e IFace2.

El [**atributo**](/windows/desktop/Midl/object) object identifica la interfaz como una interfaz de objeto e indica al compilador MIDL que genere código proxy/stub en lugar de códigos auxiliares de cliente y servidor RPC. Los métodos de interfaz de objeto deben tener un tipo de valor devuelto [**HRESULT**](/openspecs/windows_protocols/ms-erref/0642cb2f-2075-4469-918c-4441e69c548a)para permitir que el mecanismo RPC subyacente informe de errores de llamadas que no se completan debido a problemas de red.

El [**atributo uuid**](/windows/desktop/Midl/uuid) especifica el identificador de interfaz (IID). Cada interfaz, clase y biblioteca de tipos debe identificarse con su propio identificador único. Use la utilidad Uuidgen.exe para generar un conjunto de identificadores únicos para las interfaces y otros componentes.

La [**palabra clave interface**](/windows/desktop/Midl/interface) define el nombre de la interfaz. Todas las interfaces de objeto deben derivar, directa o indirectamente, [**de IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown).

El [**parámetro direccional**](/windows/desktop/Midl/in) especifica un parámetro establecido solo por el autor de la llamada. El [**parámetro out**](/windows/desktop/Midl/out-idl) especifica los datos que se pasan al autor de la llamada. El uso de ambos atributos direccionales en un parámetro especifica que el parámetro se usa tanto para enviar datos al método como para devolver los datos al autor de la llamada.

El [**atributo \_ predeterminado de**](/windows/desktop/Midl/pointer-default) puntero especifica el tipo de puntero predeterminado [**(único,**](/windows/desktop/Midl/unique) [**ref**](/windows/desktop/Midl/ref)o [**ptr)**](/windows/desktop/Midl/ptr)para todos los punteros, excepto los incluidos en las listas de parámetros. Si no se especifica ningún tipo predeterminado, MIDL supone que los punteros únicos son **únicos.** Sin embargo, si tiene varios niveles de punteros, debe especificar explícitamente un tipo de puntero predeterminado, incluso si desea que el tipo predeterminado sea **único.**

En el ejemplo anterior, la matriz BkfstStuff es una matriz compatible, cuyo tamaño \[ \] se determina en tiempo de ejecución.  El [**atributo \_ max is**](/windows/desktop/Midl/max-is) especifica la variable que contiene el valor máximo para el índice de la matriz.

El [**atributo \_ size is**](/windows/desktop/Midl/size-is) también se usa para especificar el tamaño de una matriz o, como en el ejemplo anterior, varios niveles de punteros. En el ejemplo, la llamada se puede realizar sin saber de antemano cuántos datos se devolverán.

## <a name="example2idl"></a>Example2.idl

En el siguiente ejemplo de IDL (que reutiliza las interfaces descritas en el ejemplo de IDL anterior) se muestran las distintas maneras de generar información de biblioteca de tipos para interfaces.

``` syntax
//
// Example2.idl
//

import "example.idl","oaidl.idl"; 

[
uuid(a03d1422-b1ec-11d0-8c3a-00c04fc31d2f),
helpstring("IFace3 interface"),
pointer_default(unique);
dual,
oleautomation
] 
interface IFace3 : IDispatch
{
   HRESULT MethodD([in] BSTR OrderIn,
                   [out, retval] * pTakeOut);
}; //end IFace3 def

[
uuid(a03d1423-b1ec-11d0-8c3a-00c04fc31d2f),
version(1.0),
helpstring("Example Type Library"),
] library ExampleLib
{
  importlib("stdole32.tlb");
  interface IFace3;
  [
  uuid(a03d1424-b1ec-11d0-8c3a-00c04fc31d2f),
  helpstring("Breakfast Component Class")
  ] coclass BkfstComponent
    {
    [default]interface IFace1;
    interfaceIFace2
    }; //end coclass def

[
uuid(a03d1424-b1ec-11d0-8c3a-00c04fc31d2f),
helpstring("IFace4 interface"),
pointer_default(unique);
dual,
oleautomation
] 
interface IFace4 : IDispatch
{
[propput] HRESULT MethodD([in] BSTR OrderIn);
[propget] HRESULT MethodE([out, retval] * pTakeOut);
}; //end IFace4 def
 
}; //end library def
 
```

El [**atributo helpstring**](/windows/desktop/Midl/helpstring) es opcional; se usa para describir brevemente el objeto o para proporcionar una línea de estado. Estas cadenas de ayuda son legibles con un explorador de objetos como el proporcionado con Microsoft Visual Basic.

El [**atributo**](/windows/desktop/Midl/dual) dual en IFace3 crea una interfaz que es una interfaz de distribución y una interfaz COM. Dado que se deriva de **IDispatch,** una interfaz dual admite Automation, que es lo que especifica el atributo [**oleautomation.**](/windows/desktop/Midl/oleautomation) IFace3 importa Oaidl.idl para obtener la definición de **IDispatch**.

La [**instrucción**](/windows/desktop/Midl/library) library define la biblioteca de tipos ExampleLib, que tiene sus propios [**atributos uuid,**](/windows/desktop/Midl/uuid) [**helpstring**](/windows/desktop/Midl/helpstring)y [**version.**](/windows/desktop/Midl/version)

Dentro de la definición de la biblioteca de tipos, [**la directiva importlib**](/windows/desktop/Midl/importlib) incorpora una biblioteca de tipos compilada. Todas las definiciones de biblioteca de tipos deben incluir la biblioteca de tipos base definida en Stdole32.tlb.

Esta definición de biblioteca de tipos muestra tres maneras diferentes de incluir interfaces en la biblioteca de tipos. IFace3 se incluye simplemente haciendo referencia a él dentro de la instrucción de biblioteca.

La [**instrucción coclass**](/windows/desktop/Midl/coclass) define una clase de componente completamente nueva, BkfstComponent, que incluye dos interfaces definidas previamente, IFace1 e IFace2. El atributo predeterminado designa IFace1 como interfaz predeterminada.

IFace4 se describe en la instrucción de biblioteca. El [**atributo propput**](/windows/desktop/Midl/propput) en MethodD indica que el método realiza una acción set en una propiedad del mismo nombre. El [**atributo propget**](/windows/desktop/Midl/propget) indica que el método recupera información de una propiedad del mismo nombre que el método . El [**atributo retval**](/windows/desktop/Midl/retval) de MethodD designa un parámetro de salida que contiene el valor devuelto de la función.

 

 
