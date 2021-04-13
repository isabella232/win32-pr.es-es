---
title: Anatomía de un archivo IDL
description: En estos archivos IDL de ejemplo se muestran las construcciones fundamentales de la definición de interfaz.
ms.assetid: 9c276b8a-5342-4c09-91a7-c9a9f0f83c73
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acbcfbf5c145a1fb389cc26543cf75d8cc75a107
ms.sourcegitcommit: 5ebaf3a456bc68cd0c6bd46c8135b67b1bf6fa54
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/09/2021
ms.locfileid: "104361801"
---
# <a name="anatomy-of-an-idl-file"></a>Anatomía de un archivo IDL

En estos archivos IDL de ejemplo se muestran las construcciones fundamentales de la definición de interfaz. La asignación de memoria, la serialización personalizada y la mensajería asincrónica son solo algunas de las características que se pueden implementar en una interfaz COM personalizada. Los atributos MIDL se utilizan para definir interfaces COM. Para obtener más información sobre la implementación de interfaces y bibliotecas de tipos, incluido un resumen de los atributos MIDL, vea [definiciones de interfaz y bibliotecas de tipos](/windows/desktop/Midl/interface-definitions-and-type-libraries) en la guía y referencia del programador de MIDL. Para obtener una referencia completa de todos los atributos, palabras clave y directivas de MIDL, vea la [Referencia del lenguaje MIDL](/windows/desktop/Midl/midl-language-reference).

## <a name="exampleidl"></a>Ejemplo. idl

En el siguiente archivo IDL de ejemplo se definen dos interfaces COM. A partir de este archivo IDL, Midl.exe generará código proxy/código auxiliar y archivos de encabezado y serialización. Una sección de línea por línea sigue el ejemplo.

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

La instrucción de [**importación**](/windows/desktop/Midl/import) IDL se usa aquí para traer un archivo de encabezado, Mydefs. h, que contiene los tipos definidos por el usuario, y Unknwn. idl, que contiene la definición de [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown), de la que se derivan IFace1 y IFace2.

El atributo de [**objeto**](/windows/desktop/Midl/object) identifica la interfaz como una interfaz de objeto e indica al compilador de MIDL que genere código de proxy/código auxiliar en lugar del cliente RPC y los códigos auxiliares de servidor. Los métodos de la interfaz de objeto deben tener un tipo de valor devuelto de [**HRESULT**](/openspecs/windows_protocols/ms-erref/0642cb2f-2075-4469-918c-4441e69c548a), para permitir que el mecanismo RPC subyacente informe de los errores de las llamadas que no se han podido completar debido a problemas de red.

El atributo [**UUID**](/windows/desktop/Midl/uuid) especifica el identificador de interfaz (IID). Cada interfaz, clase y biblioteca de tipos debe identificarse con su propio identificador único. Use el Uuidgen.exe de la utilidad para generar un conjunto de identificadores únicos para las interfaces y otros componentes.

La palabra clave [**interface**](/windows/desktop/Midl/interface) define el nombre de la interfaz. Todas las interfaces de objeto deben derivar, directa o indirectamente, de [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown).

El parámetro [**en**](/windows/desktop/Midl/in) direccional especifica un parámetro que solo el autor de la llamada establece. El parámetro [**out**](/windows/desktop/Midl/out-idl) especifica los datos que se devuelven al autor de la llamada. El uso de ambos atributos direccionales en un parámetro especifica que el parámetro se utiliza para enviar datos al método y para devolver datos al llamador.

El [**atributo \_ default del puntero**](/windows/desktop/Midl/pointer-default) especifica el tipo de puntero predeterminado ([**Unique**](/windows/desktop/Midl/unique), [**ref**](/windows/desktop/Midl/ref)o [**ptr**](/windows/desktop/Midl/ptr)) de todos los punteros excepto los incluidos en las listas de parámetros. Si no se especifica ningún tipo predeterminado, MIDL supone que los punteros simples son **únicos**. Sin embargo, si tiene varios niveles de punteros, debe especificar explícitamente un tipo de puntero predeterminado, incluso si desea que el tipo predeterminado sea **único**.

En el ejemplo anterior, la matriz BkfstStuff \[ \] es una *matriz compatible*, cuyo tamaño se determina en tiempo de ejecución. El atributo [**Max \_ is**](/windows/desktop/Midl/max-is) especifica la variable que contiene el valor máximo para el índice de la matriz.

El atributo [**size \_ también se**](/windows/desktop/Midl/size-is) utiliza para especificar el tamaño de una matriz o, como en el ejemplo anterior, varios niveles de punteros. En el ejemplo, se puede realizar la llamada sin conocer de antemano la cantidad de datos que se devolverá.

## <a name="example2idl"></a>Example2. idl

En el siguiente ejemplo de IDL (que reutiliza las interfaces descritas en el ejemplo IDL anterior) se muestran las distintas formas de generar información de la biblioteca de tipos para las interfaces.

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

El atributo [**HelpString**](/windows/desktop/Midl/helpstring) es opcional; se usa para describir brevemente el objeto o para proporcionar una línea de estado. Estas cadenas de ayuda se pueden leer con un examinador de objetos como el que se proporciona con Microsoft Visual Basic.

El atributo [**dual**](/windows/desktop/Midl/dual) de IFace3 crea una interfaz que es una interfaz de envío y una interfaz com. Dado que se deriva de **IDispatch**, una interfaz dual admite automatización, que es lo que especifica el atributo [**oleautomation**](/windows/desktop/Midl/oleautomation) . IFace3 importa Oaidl. idl para obtener la definición de **IDispatch**.

La instrucción [**Library**](/windows/desktop/Midl/library) define la biblioteca de tipos ExampleLib, que tiene sus propios atributos [**UUID**](/windows/desktop/Midl/uuid), [**HelpString**](/windows/desktop/Midl/helpstring)y [**version**](/windows/desktop/Midl/version) .

Dentro de la definición de la biblioteca de tipos, la directiva [**importlib**](/windows/desktop/Midl/importlib) se coloca en una biblioteca de tipos compilada. Todas las definiciones de biblioteca de tipos deben incorporar la biblioteca de tipos base definida en Stdole32. tlb.

Esta definición de biblioteca de tipos muestra tres formas diferentes de incluir interfaces en la biblioteca de tipos. IFace3 se incluye simplemente haciendo referencia a él en la instrucción Library.

La instrucción [**CoClass**](/windows/desktop/Midl/coclass) define una clase de componente completamente nueva, BkfstComponent, que incluye dos interfaces definidas previamente, IFace1 y IFace2. El atributo default designa IFace1 como la interfaz predeterminada.

IFace4 se describe en la instrucción Library. El atributo [**PROPPUT**](/windows/desktop/Midl/propput) en el método indica que el método realiza una acción set en una propiedad con el mismo nombre. El atributo [**propget**](/windows/desktop/Midl/propget) indica que el método recupera información de una propiedad con el mismo nombre que el método. El atributo [**retval**](/windows/desktop/Midl/retval) de methoded designa un parámetro de salida que contiene el valor devuelto de la función.

 

 
