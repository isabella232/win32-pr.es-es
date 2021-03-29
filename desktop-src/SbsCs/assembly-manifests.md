---
description: Un manifiesto de ensamblado es un archivo XML que describe un ensamblado en paralelo.
ms.assetid: f7973019-0a80-498e-adf1-c66267c813f4
title: Manifiestos de ensamblado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 254702d5044331fa5d47def815556dbd8edef2f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277355"
---
# <a name="assembly-manifests"></a>Manifiestos de ensamblado

Un manifiesto de ensamblado es un archivo XML que describe un ensamblado en paralelo. Los manifiestos de ensamblado describen los nombres y las versiones de los ensamblados en paralelo, los archivos y los recursos del ensamblado, así como la dependencia del ensamblado en otros ensamblados en paralelo. La correcta instalación, activación y ejecución de ensamblados en paralelo requiere que el manifiesto del ensamblado acompañe siempre a un ensamblado del sistema.

Para obtener una lista completa del esquema XML, consulte [esquema del archivo de manifiesto](manifest-file-schema.md).

Los manifiestos de ensamblado tienen los siguientes elementos y atributos.



| Elemento                           | Atributos                | Obligatorio |
|-----------------------------------|---------------------------|----------|
| **assembl**                      |                           | Sí      |
|                                   | **manifestVersion**       | Sí      |
| **no se pudo heredar**                 |                           | No       |
| **assemblyIdentity**              |                           | Sí      |
|                                   | **type**                  | Sí      |
|                                   | **name**                  | Sí      |
|                                   | **language**              | No       |
|                                   | **processorArchitecture** | No       |
|                                   | **version**               | Sí      |
|                                   | **publicKeyToken**        | No       |
| **pendiente**                    |                           | No       |
| **dependentAssembly**             |                           | No       |
| **file**                          |                           | No       |
|                                   | **name**                  | Sí      |
|                                   | **hashalg**               | No       |
|                                   | **hash**                  | No       |
| **comclase**                      |                           | No       |
|                                   | **description**           | No       |
|                                   | **CLSID**                 | Sí      |
|                                   | **threadingModel**        | No       |
|                                   | **tlbid**                 | No       |
|                                   | **Programa**                | No       |
|                                   | **miscStatus**            | No       |
|                                   | **miscStatusIcon**        | No       |
|                                   | **miscStatusContent**     | No       |
|                                   | **miscStatusDocPrint**    | No       |
|                                   | **miscStatusDocPrint**    | No       |
| **typelib**                       |                           | No       |
|                                   | **tlbid**                 | Sí      |
|                                   | **version**               | Sí      |
|                                   | **helpDir**               | Sí      |
|                                   | **identificador**            | No       |
|                                   | **flags**                 | No       |
| **comInterfaceExternalProxyStub** |                           | No       |
|                                   | **suscripto**                   | Sí      |
|                                   | **baseInterface**         | No       |
|                                   | **numMethods**            | No       |
|                                   | **name**                  | No       |
|                                   | **tlbid**                 | No       |
|                                   | **proxyStubClsid32**      | No       |
| **comInterfaceProxyStub**         |                           | No       |
|                                   | **suscripto**                   | Sí      |
|                                   | **name**                  | Sí      |
|                                   | **tlbid**                 | No       |
|                                   | **baseInterface**         | No       |
|                                   | **numMethods**            | No       |
|                                   | **proxyStubClsid32**      | No       |
|                                   | **threadingModel**        | No       |
| **windowClass**                   |                           | No       |
|                                   | **versiones del**             | No       |



 

## <a name="file-location"></a>Ubicación del archivo

Los manifiestos de ensamblado se pueden instalar en tres ubicaciones:

-   Como manifiestos que acompañan a los [ensamblados compartidos](/windows/desktop/Msi/shared-assemblies), los manifiestos de ensamblado deben instalarse como un archivo independiente en la caché de ensamblados en paralelo. Esta suele ser la carpeta WinSxS en el directorio de Windows.
-   Como manifiestos que acompañan a los [ensamblados privados](/windows/desktop/Msi/private-assemblies), los manifiestos de ensamblado deben instalarse en la estructura de directorios de la aplicación. Suele ser un archivo independiente en la misma carpeta que el archivo ejecutable de la aplicación.
-   Como recurso en un archivo DLL, el ensamblado está disponible para el uso privado del archivo DLL. Un manifiesto de ensamblado no se puede incluir como un recurso en un archivo EXE. Un archivo EXE puede incluir un [manifiesto de aplicación](application-manifests.md) como un recurso.

## <a name="file-name-syntax"></a>Sintaxis de los nombres de archivo

El nombre de un manifiesto del ensamblado es cualquier nombre de archivo válido seguido de. manifest.

Por ejemplo, un manifiesto de ensamblado que hace referencia a myAssembly usaría la siguiente sintaxis de nombre de archivo. Puede omitir el campo <*ID. de recurso*> si el manifiesto del ensamblado se instala como un archivo independiente o si el identificador de recurso es 1.

<dl> myAssembly. <resource ID> . manifiesto
</dl>

> [!Note]  
> Debido a las búsquedas en paralelo de ensamblados privados, se aplican las siguientes restricciones de nomenclatura al empaquetar un archivo DLL como ensamblado privado. Una manera recomendada de hacerlo es colocar el manifiesto del ensamblado en el archivo DLL como un recurso. En este caso, el identificador de recurso debe ser igual a 1 y el nombre del ensamblado privado puede ser el mismo que el nombre del archivo DLL. Por ejemplo, si el nombre del archivo DLL es Microsoft.Windows.mysample.dll, el valor del atributo name usado en el elemento **assemblyIdentity** del manifiesto también puede ser Microsoft. Windows. sample. Una manera alternativa consiste en colocar el manifiesto del ensamblado en un archivo independiente. En este caso, el nombre del ensamblado y su manifiesto deben ser diferentes del nombre del archivo DLL. Por ejemplo, Microsoft. Windows. mysampleAsm, Microsoft. Windows. mysampleAsm. manifest y Microsoft.Windows.Mysample.dll. Para obtener más información sobre cómo las búsquedas en paralelo de ensamblados privados, vea [secuencia de búsqueda de ensamblados](assembly-searching-sequence.md).

 

## <a name="elements"></a>Elementos

Los nombres de los elementos y atributos distinguen mayúsculas de minúsculas. Los valores de los elementos y atributos no distinguen mayúsculas de minúsculas, excepto el valor del atributo type.

<dl> <dt>

<span id="assembly"></span><span id="ASSEMBLY"></span>**assembl**
</dt> <dd>

Elemento contenedor. Su primer subelemento debe ser un elemento **assemblyIdentity** o **noinheritable** . El manifiesto del ensamblado describe de forma única el ensamblado en paralelo identificado por **assemblyIdentity**. Obligatorio.

El elemento de ensamblado debe estar en el espacio de nombres "urn: schemas-microsoft-com: ASM. v1". Los elementos secundarios del ensamblado también deben estar en este espacio de nombres, por herencia o mediante el etiquetado.

El elemento **Assembly** tiene el siguiente atributo.



| Atributo           | Descripción                                           |
|---------------------|-------------------------------------------------------|
| **manifestVersion** | El atributo **manifestVersion** debe establecerse en 1,0. |



 

</dd> <dt>

<span id="noInheritable"></span><span id="noinheritable"></span><span id="NOINHERITABLE"></span>**no se pudo heredar**
</dt> <dd>

Incluya este elemento en un manifiesto del ensamblado para indicar que el ensamblado administra los [contextos de activación](activation-contexts.md) y sus objetos. El elemento **Noinheritable** debe ser un subelemento de un elemento **Assembly** . El elemento **assemblyIdentity** debe aparecer después de cualquier elemento que se haya **heredado** . El elemento **Noinheritable** es necesario en el manifiesto del ensamblado si el ensamblado lo usa cualquier [manifiesto de aplicación](application-manifests.md) que incluya el elemento **NoInherit** . Un elemento **Noinheritable** en un manifiesto de aplicación no tiene ningún efecto. Un elemento **Noinheritable** no tiene elementos secundarios.

</dd> <dt>

<span id="assemblyIdentity"></span><span id="assemblyidentity"></span><span id="ASSEMBLYIDENTITY"></span>**assemblyIdentity**
</dt> <dd>

Describe e identifica de forma única un ensamblado en paralelo.

Como primer subelemento de un elemento **Assembly** , **assemblyIdentity** describe e identifica de forma única el ensamblado en paralelo que posee este manifiesto del ensamblado. Esto se denomina **assemblyIdentity** de Def-context del manifiesto del ensamblado.

Como primer subelemento de un elemento **dependentAssembly** , **assemblyIdentity** describe e identifica de forma única un ensamblado en paralelo que usa el elemento **assemblyIdentity** de Def-context. Esto se denomina el método **assemblyIdentity** de contexto de referencia del manifiesto del ensamblado. El ensamblado DEF-context requiere que el ensamblado de contexto de referencia funcione correctamente. Tenga en cuenta que cada **assemblyIdentity** del contexto de referencia debe coincidir exactamente con el **assemblyIdentity** de Def-context correspondiente en el manifiesto del ensamblado del ensamblado de referencia.

Este elemento no tiene subelementos. El elemento **assemblyIdentity** tiene los atributos siguientes.



| Atributo                 | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                               |
|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **type**                  | Especifica el tipo de ensamblado. El valor debe ser Win32 y en minúsculas. Obligatorio.                                                                                                                                                                                                                                                                                                                                                         |
| **name**                  | Designa de forma única el ensamblado. Use el siguiente formato para el nombre de ensamblado: Organization.Division.Name. Por ejemplo, Microsoft. Windows. mysampleAsm. Obligatorio. Tenga en cuenta que en el caso de una DLL empaquetada como un ensamblado privado con un archivo de manifiesto independiente, el nombre del ensamblado debe ser diferente del nombre del archivo DLL y del manifiesto.<br/>                                                                              |
| **language**              | Identifica el idioma del ensamblado. Opcional. Si el ensamblado es específico del idioma, especifique el código de lenguaje DHTML. En el **assemblyIdentity** de Def-context de un manifiesto de ensamblado diseñado para uso internacional (idioma neutro), omita el atributo Language.<br/> En un grupo de referencias de referencia **assemblyIdentity** de un manifiesto de ensamblado diseñado para uso internacional (idioma neutro), establezca el valor de Language en " \* ".<br/> |
| **processorArchitecture** | Especifica el procesador. Los valores válidos son x86 para Windows de 32 bits e ia64 para Windows de 64 bits. Opcional.                                                                                                                                                                                                                                                                                                                               |
| **version**               | Especifica la versión del ensamblado. Use el formato de versión de cuatro partes: mmmmm. nnnnn. ooooo. ppppp. Cada una de las partes separadas por puntos puede ser 0-65535, ambos inclusive. Para obtener más información, vea [versiones de ensamblado](assembly-versions.md). Obligatorio.                                                                                                                                                                                               |
| **publicKeyToken**        | Cadena hexadecimal de 16 caracteres que representa los últimos 8 bytes del hash SHA-1 de la clave pública con la que se firma el ensamblado. La clave pública que se usa para firmar el catálogo debe ser de 2048 bits o superior. Se requiere para los ensamblados en paralelo compartidos.                                                                                                                                                                                |



 

</dd> <dt>

<span id="dependency"></span><span id="DEPENDENCY"></span>**pendiente**
</dt> <dd>

Un elemento contenedor que incluye al menos un elemento **dependentAssembly**. El primer subelemento debe ser un elemento **dependentAssembly** . Una **dependencia** no tiene atributos. Opcional.

</dd> <dt>

<span id="dependentAssembly"></span><span id="dependentassembly"></span><span id="DEPENDENTASSEMBLY"></span>**dependentAssembly**
</dt> <dd>

El primer subelemento debe ser un elemento **assemblyIdentity** que describe e identifica de forma única un ensamblado en paralelo que usa el ensamblado en paralelo que posee este manifiesto del ensamblado. Cada **dependentAssembly** debe estar dentro de una **dependencia** exactamente. Opcional.

</dd> <dt>

<span id="file"></span><span id="FILE"></span>**filesystem**
</dt> <dd>

Contiene archivos usados por un ensamblado en paralelo. Contiene **subclases**, **typelib**, **windowClass**, **comInterfaceProxyStub** subelementos. Opcional.

El elemento **File** tiene los atributos siguientes.



| Atributo   | Descripción                                                                                             |
|-------------|---------------------------------------------------------------------------------------------------------|
| **name**    | Nombre del archivo, por ejemplo, Conctl32.dll.                                                            |
| **hashalg** | Algoritmo usado para crear un hash del archivo. Este valor debe ser SHA1.                                 |
| **hash**    | Un hash del archivo al que se hace referencia por nombre. Cadena hexadecimal de longitud según el algoritmo hash. |



 

</dd> <dt>

<span id="comClass"></span><span id="comclass"></span><span id="COMCLASS"></span>**comclase**
</dt> <dd>

Un subelemento de un elemento **File** . Opcional.

El elemento **comClass** tiene los siguientes atributos.



| Atributo               | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **description**         | Nombre de clase.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| **CLSID**               | GUID que identifica de forma única la clase. Obligatorio. El valor debe estar en el formato de un GUID válido.                                                                                                                                                                                                                                                                                                                                                                                                                             |
| **threadingModel**      | Modelo de subprocesos utilizado por las clases COM en proceso. Si esta propiedad es null, no se utiliza ningún modelo de subprocesos. El componente se crea en el subproceso principal del cliente y las referencias de otros subprocesos se serializan en este subproceso. Opcional. Los valores válidos son: "Apartment", "Free", "both" y "neutral".                                                                                                                                                                                                                         |
| **tlbid**               | GUID de la biblioteca de tipos para este componente COM. El valor debe estar en el formato de un GUID. Opcional.                                                                                                                                                                                                                                                                                                                                                                                                                              |
| **Programa**              | Identificador de programación dependiente de la versión asociado al componente COM. El formato de un ProgID es <el *componente*> de *proveedor* . <>. <*versión*>.                                                                                                                                                                                                                                                                                                                                                                      |
| **miscStatus**          | Los duplicados en el manifiesto de ensamblado proporcionan la información proporcionada por la clave del registro MiscStatus. Si no se encuentran los valores de los atributos **miscStatusIcon**, **miscStatusContent**, **miscStatusDocprint** o **miscStatusThumbnail** , se usa el valor predeterminado correspondiente indicado en **miscStatus** para los atributos que faltan. El valor puede ser una lista delimitada por comas de los valores de atributo de la tabla siguiente. Puede usar este atributo si la clase COM es una clase OCX que requiere valores de clave del registro Miscstatus. |
| **miscStatusIcon**      | En el manifiesto del ensamblado se incluye la información proporcionada por el icono de DVASPECT \_ . Puede proporcionar un icono de un objeto. El valor puede ser una lista delimitada por comas de los valores de atributo de la tabla siguiente. Puede usar este atributo si la clase COM es una clase OCX que requiere valores de clave del registro Miscstatus.                                                                                                                                                                                                                |
| **miscStatusContent**   | Los duplicados en el ensamblado manifiestan la información proporcionada por el contenido de DVASPECT \_ . Puede proporcionar un documento compuesto que se pueda mostrar en una pantalla o una impresora. El valor puede ser una lista delimitada por comas de los valores de atributo de la tabla siguiente. Puede usar este atributo si la clase COM es una clase OCX que requiere valores de clave del registro Miscstatus.                                                                                                                                                                          |
| **miscStatusDocprint**  | Los duplicados en el ensamblado proporcionan la información proporcionada por DVASPECT \_ DOCPRINT. Puede proporcionar una representación de objeto que se pueda mostrar en la pantalla como si se imprimiera en una impresora. El valor puede ser una lista delimitada por comas de los valores de atributo de la tabla siguiente. Puede usar este atributo si la clase COM es una clase OCX que requiere valores de clave del registro Miscstatus.                                                                                                                                               |
| **miscStatusThumbnail** | Los duplicados de un ensamblado manifiestan la información proporcionada por la miniatura de DVASPECT \_ . Puede proporcionar una miniatura de un objeto que se pueda mostrar en una herramienta de exploración. El valor puede ser una lista delimitada por comas de los valores de atributo de la tabla siguiente. Puede usar este atributo si la clase COM es una clase OCX que requiere valores de clave del registro Miscstatus.                                                                                                                                                                         |



 

El elemento **comClass** puede tener los elementos <progid>...</progid> como elementos secundarios, que muestran los ProgID dependientes de la versión.

En el ejemplo siguiente se muestra un elemento **comClass** incluido en un elemento **File** .

``` syntax
<file name="sampleu.dll">
        <comClass description="Font Property Page"
    clsid="{0BE35200-8F91-11CE-9DE3-00AA004BB851}"
          threadingModel = "Both"
             tlbid = "{44EC0535-400F-11D0-9DCD-00A0C90391D3}"/>
        <comClass description="Color Property Page"
    clsid="{0BE35201-8F91-11CE-9DE3-00AA004BB851}" 
    progid="ABC.Registrar"/>
    </file>
```

Si la clase COM es una clase OCX que requiere que la subclave del registro MiscStatus especifique cómo crear y mostrar un objeto, puede habilitar el objeto duplicando esta información en el manifiesto del ensamblado. Especifique las características del objeto mediante los atributos **miscStatus**, **miscStatusIcon**, **miscStatusContent**, **miscStatusDocprint** y **miscStatusThumbnail** del elemento **comClass** . Establezca estos atributos en una lista separada por comas de valores de atributo de la tabla siguiente. Estos atributos duplican la información que proporcionaría una enumeración DVASPECT. Si no se encuentra ningún valor para **miscStatusIcon**, **miscStatusContent**, **miscStatusDocprint** o **miscStatusThumbnail**, se usan los valores predeterminados especificados en **miscStatus** . Utilice los valores de atributo de la tabla siguiente. Estos se corresponden con las marcas de bits de una enumeración [**OLEMISC**](/windows/win32/api/oleidl/ne-oleidl-olemisc) .



| Valor del atributo              | OLEMISC constante)                      |
|------------------------------|---------------------------------------|
| recomposeonresize            | OLEMISC \_ RECOMPOSEONRESIZE            |
| onlyiconic                   | OLEMISC \_ ONLYICONIC                   |
| insertnotreplace             | OLEMISC \_ INSERTNOTREPLACE             |
| static                       | \_estático OLEMISC                       |
| cantlinkinside               | OLEMISC \_ CANTLINKINSIDE               |
| canlinkbyole1                | OLEMISC \_ CANLINKBYOLE1                |
| islinkobject                 | OLEMISC \_ ISLINKOBJECT                 |
| insideout                    | OLEMISC \_ InsideOut                    |
| activatewhenvisible          | OLEMISC \_ ACTIVATEWHENVISIBLE          |
| renderingisdeviceindependent | OLEMISC \_ RENDERINGISDEVICEINDEPENDENT |
| invisibleatruntime           | OLEMISC \_ INVISIBLEATRUNTIME           |
| alwaysrun                    | OLEMISC \_ ALWAYSRUN                    |
| actslikebutton               | OLEMISC \_ ACTSLIKEBUTTON               |
| actslikelabel                | OLEMISC \_ ACTSLIKELABEL                |
| nouiactivate                 | OLEMISC \_ NOUIACTIVATE                 |
| alineable                    | OLEMISC \_ alineable                    |
| simpleframe                  | OLEMISC \_ SIMPLEFRAME                  |
| setclientsitefirst           | OLEMISC \_ SETCLIENTSITEFIRST           |
| IMEMode                      | TOLEMISC \_ IMEMODE                     |
| ignoreativatewhenvisible     | OLEMISC \_ IGNOREACTIVATEWHENVISIBLE    |
| wantstomenumerge             | OLEMISC \_ WANTSTOMENUMERGE             |
| supportsmultilevelundo       | OLEMISC \_ SUPPORTSMULTILEVELUNDO       |



 

</dd> <dt>

<span id="typelib"></span><span id="TYPELIB"></span>**typelib**
</dt> <dd>

Un subelemento de un elemento **File** . Opcional.

El elemento **typelib** tiene los atributos que se muestran en la tabla siguiente.



| Atributo      | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                     |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **tlbid**      | IDENTIFICADOR único de la biblioteca de tipos. Obligatorio.                                                                                                                                                                                                                                                                                                                                                                                    |
| **version**    | Número de versión de dos partes de la biblioteca de tipos. Si solo aumenta el número de versión secundaria, todas las características de la biblioteca de tipos anterior se admiten de una manera compatible. Si cambia el número de versión principal, se debe volver a compilar el código compilado con la biblioteca de tipos. El número de versión de la biblioteca de tipos puede diferir del número de versión de la aplicación. Obligatorio.                                      |
| **helpDir**    | Directorio donde se encuentra el archivo de ayuda para los tipos de la biblioteca de tipos. Si la aplicación admite bibliotecas de tipos para varios idiomas, es posible que las bibliotecas hagan referencia a distintos nombres de archivo en el directorio del archivo de ayuda. Si no hay ningún valor, especifique "". Obligatorio.                                                                                                                                                          |
| **identificador** | Representación de cadena hexadecimal del identificador de configuración regional (LCID). Es de uno a cuatro dígitos hexadecimales sin prefijo 0x y sin ceros a la izquierda. El LCID puede tener un identificador de subidioma neutro. Para obtener más información, vea [identificadores de configuración regional](/windows/desktop/Intl/locale-identifiers). Opcional.                                                                                                                                      |
| **flags**      | Representación de cadena de las marcas de la biblioteca de tipos para esta biblioteca de tipos. En concreto, debe ser "restricted", "CONTROL", "HIDDEN" y "HASDISKIMAGE". Estos son los valores de la enumeración [**LIBFLAGS**](/windows/win32/api/oaidl/ne-oaidl-libflags) y son las mismas marcas especificadas en el parámetro *ULibFlags* del método [**ICreateTypeLib:: SetLibFlags**](/windows/win32/api/oaidl/nf-oaidl-icreatetypelib-setlibflags) . Opcional. |



 

En el ejemplo siguiente se muestra un elemento **typelib** incluido en un elemento **File** .

``` syntax
<file name="sampleu.dll">
       <typelib tlbid="{44EC0535-400F-11D0-9DCD-00A0C90391D3}"
       version="1.0" helpdir=""/>
</file>
```

</dd> <dt>

<span id="comInterfaceExternalProxyStub"></span><span id="cominterfaceexternalproxystub"></span><span id="COMINTERFACEEXTERNALPROXYSTUB"></span>**comInterfaceExternalProxyStub**
</dt> <dd>

**ComInterfaceExternalProxyStub** es un subelemento de un elemento **Assembly** y se utiliza para las interfaces de automatización. Por ejemplo, [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) y sus interfaces derivadas. Opcional.

La implementación de código auxiliar de proxy predeterminada es adecuada para la mayoría de las interfaces de automatización, como las interfaces derivadas de [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch). El código auxiliar del proxy de interfaz y todas las demás implementaciones externas de la interfaz de código auxiliar de proxy deben aparecer en **comInterfaceExternalProxyStub**. El elemento **comInterfaceExternalProxyStub** tiene los atributos que se muestran en la tabla siguiente.



| Atributo         | Descripción                                                                                                                                                                                 |
|-------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **suscripto**           | IID de la interfaz para la que se declara el proxy. Obligatorio. El valor debe tener el formato: "{IID}".                                                                         |
| **baseInterface** | El IID de la interfaz de la que se deriva el que describe el atributo **IID** . Este atributo es opcional. El valor debe tener el formato: "{IID}".                            |
| **numMethods**    | El número de métodos implementados por la interfaz. Este atributo es opcional. El valor debe tener el formato: "n".                                                                       |
| **name**          | Nombre de la interfaz tal y como aparecería en el código. Por ejemplo, "IViewObject". No debe ser una cadena descriptiva. Este atributo es opcional. El valor debe tener el formato: "nombre". |
| **tlbid**         | Biblioteca de tipos que contiene la descripción de la interfaz especificada por el atributo **IID** . Este atributo es opcional. El valor debe tener el formato: "{TLBID}".                |
| proxyStubClsid32  | Asigna un IID a un CLSID en dll de proxy de 32 bits.                                                                                                                                                |



 

En el ejemplo siguiente se muestra un elemento **comInterfaceExternalProxyStub** .

``` syntax
<comInterfaceExternalProxyStub 
  name="IAxWinAmbientDispatch" 
    iid="{B6EA2051-048A-11D1-82B9-00C04FB9942E}" 
    numMethods="35" 
  baseInterface="{00000000-0000-0000-C000-000000000046}"/>
```

</dd> <dt>

<span id="comInterfaceProxyStub"></span><span id="cominterfaceproxystub"></span><span id="COMINTERFACEPROXYSTUB"></span>**comInterfaceProxyStub**
</dt> <dd>

Un subelemento de un elemento **File** . Opcional.

Si un archivo del ensamblado implementa un código auxiliar de proxy, la etiqueta de archivo correspondiente debe incluir un subelemento **comInterfaceProxyStub** que tenga atributos idénticos a un elemento **comInterfaceProxyStub** . La serialización de interfaces entre procesos y subprocesos puede no funcionar según lo esperado si omite algunas de las dependencias de **comInterfaceProxyStub** para el componente.

El elemento **comInterfaceProxyStub** tiene los siguientes atributos.



| Atributo            | Descripción                                                                                                                                                                                                                                                                                                 |
|----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **suscripto**              | El. IID de la interfaz para la que se declara el proxy. Obligatorio. El valor debe tener el formato: "{IID}".                                                                                                                                                                                        |
| **name**             | Nombre de la interfaz tal y como aparecería en el código. Por ejemplo, "IViewObject". No debe ser una cadena descriptiva. Este atributo es opcional. El valor debe tener el formato: "nombre".                                                                                                                 |
| **tlbid**            | Biblioteca de tipos que contiene la descripción de la interfaz especificada por el atributo **IID** . Este atributo es opcional. El valor debe tener el formato: "{TLBID}".                                                                                                                                 |
| **baseInterface**    | El IID de la interfaz de la que se deriva el que describe el atributo **IID** . Este atributo es opcional. El valor debe tener el formato: "{IID}".                                                                                                                                            |
| **numMethods**       | El número de métodos implementados por la interfaz. Este atributo es opcional. El valor debe tener el formato: "n".                                                                                                                                                                                       |
| **proxyStubClsid32** | Asigna un IID a un CLSID en dll de proxy de 32 bits.                                                                                                                                                                                                                                                                |
| **threadingModel**   | Modelo de subprocesos utilizado por las clases COM en proceso. Si esta propiedad es null, no se utiliza ningún modelo de subprocesos. El componente se crea en el subproceso principal del cliente y las referencias de otros subprocesos se serializan en este subproceso. Opcional. Los valores válidos son: "Apartment", "Free", "both" y "neutral". |



 

</dd> <dt>

<span id="windowclass"></span><span id="WINDOWCLASS"></span>**windowclass**
</dt> <dd>

Nombre de una clase de Windows de la que se va a crear una versión. El elemento **windowclass** tiene el siguiente atributo.



| Atributo     | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **versiones del** | Este atributo controla si el nombre de la clase de ventana interna utilizada en el registro contiene la versión del ensamblado que contiene la clase de ventana. El valor de este atributo puede ser "Yes" o "no". El valor predeterminado es "sí". Solo se debe usar el valor "no" si la misma clase de ventana está definida por un componente en paralelo y un componente no en paralelo equivalente y desea tratarlos como la misma clase de ventana. Tenga en cuenta que las reglas habituales sobre el registro de clases de ventana solo se aplican el primer componente que registra la clase de ventana podrá registrarla, ya que no tiene versiones. |



 

En el ejemplo siguiente se muestra un elemento **windowclass** incluido en un elemento **File** .

``` syntax
<file name="comctl32.dll">
        <windowClass versioned="no">ToolbarWindow32</windowClass>
</file>
```

</dd> </dl>

## <a name="example"></a>Ejemplo

El siguiente es un ejemplo de manifiesto del ensamblado.

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" 
manifestVersion="1.0">
    <assemblyIdentity type="win32" name="Microsoft.Tools.SampleAssembly" version="6.0.0.0" processorArchitecture="x86" publicKeyToken="0000000000000000"/>
    <file name="sampleu.dll" hash="3eab067f82504bf271ed38112a4ccdf46094eb5a" hashalg="SHA1">
        <comClass description="Font Property Page" clsid="{0BE35200-8F91-11CE-9DE3-00AA004BB851}"/>
        <comClass description="Color Property Page" clsid="{0BE35201-8F91-11CE-9DE3-00AA004BB851}"/>
        <comClass description="Picture Property Page" clsid="{0BE35202-8F91-11CE-9DE3-00AA004BB851}"/>
    </file>
    <file name="bar.dll" hash="ac72753e5bb20446d88a48c8f0aaae769a962338" hashalg="SHA1"/>
    <file name="foo.dll" hash="a7312a1f6cfb46433001e0540458de60adcd5ec5" hashalg="SHA1">
        <comClass description="Registrar Class" clsid="{44EC053A-400F-11D0-9DCD-00A0C90391D3}" progid="ATL.Registrar"/>
    <comInterfaceProxyStub iid="{B6EA2051-048A-11D1-82B9-00C04FB9942E}" name=" IAxWinAmbientDispatch " tlbid="{34EC053A-400F-11D0-9DCD-00A0C90391D3}"/>
        <typelib tlbid="{44EC0535-400F-11D0-9DCD-00A0C90391D3}" version="1.0" helpdir=""/>
    </file>
    <file name="sampledll.dll" hash="ba62960ceb15073d2598379307aad84f3a73dfcb" hashalg="SHA1"/>
<windowClass>ToolbarWindow32</windowClass>
        <windowClass>ComboBoxEx32</windowClass>
        <windowClass>sample_trackbar32</windowClass>
        <windowClass>sample_updown32</windowClass>
</assembly>
```

 

