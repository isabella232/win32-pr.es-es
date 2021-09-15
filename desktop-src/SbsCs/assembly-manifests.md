---
description: Un manifiesto de ensamblado es un archivo XML que describe un ensamblado en paralelo.
ms.assetid: f7973019-0a80-498e-adf1-c66267c813f4
title: Manifiestos de ensamblado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94310ce3fdbb05706f889ea9755f7a47320ada56
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127271743"
---
# <a name="assembly-manifests"></a>Manifiestos de ensamblado

Un manifiesto de ensamblado es un archivo XML que describe un ensamblado en paralelo. Los manifiestos de ensamblado describen los nombres y versiones de ensamblados en paralelo, archivos y recursos del ensamblado, así como la dependencia del ensamblado en otros ensamblados en paralelo. La instalación, activación y ejecución correctas de ensamblados en paralelo requiere que el manifiesto de ensamblado siempre acompaña a un ensamblado en el sistema.

Para obtener una lista completa del esquema XML, vea [Esquema de archivo de manifiesto.](manifest-file-schema.md)

Los manifiestos de ensamblado tienen los siguientes elementos y atributos.



| Elemento                           | Atributos                | Requerido |
|-----------------------------------|---------------------------|----------|
| **ensamblaje**                      |                           | Sí      |
|                                   | **manifestVersion**       | Sí      |
| **noInheritable**                 |                           | No       |
| **Assemblyidentity**              |                           | Sí      |
|                                   | **type**                  | Sí      |
|                                   | **name**                  | Sí      |
|                                   | **language**              | No       |
|                                   | **processorArchitecture** | No       |
|                                   | **version**               | Sí      |
|                                   | **Publickeytoken**        | No       |
| **Dependencia**                    |                           | No       |
| **dependentAssembly**             |                           | No       |
| **file**                          |                           | No       |
|                                   | **name**                  | Sí      |
|                                   | **hashalg**               | No       |
|                                   | **hash**                  | No       |
| **comClass**                      |                           | No       |
|                                   | **description**           | No       |
|                                   | **Clsid**                 | Sí      |
|                                   | **threadingModel**        | No       |
|                                   | **tlbid**                 | No       |
|                                   | **Progid**                | No       |
|                                   | **miscStatus**            | No       |
|                                   | **miscStatusIcon**        | No       |
|                                   | **miscStatusContent**     | No       |
|                                   | **miscStatusDocPrint**    | No       |
|                                   | **miscStatusDocPrint**    | No       |
| **Typelib**                       |                           | No       |
|                                   | **tlbid**                 | Sí      |
|                                   | **version**               | Sí      |
|                                   | **helpdir**               | Sí      |
|                                   | **resourceid**            | No       |
|                                   | **flags**                 | No       |
| **comInterfaceExternalProxyStub** |                           | No       |
|                                   | **Iid**                   | Sí      |
|                                   | **baseInterface**         | No       |
|                                   | **numMethods**            | No       |
|                                   | **name**                  | No       |
|                                   | **tlbid**                 | No       |
|                                   | **proxyStubClsid32**      | No       |
| **comInterfaceProxyStub**         |                           | No       |
|                                   | **Iid**                   | Sí      |
|                                   | **name**                  | Sí      |
|                                   | **tlbid**                 | No       |
|                                   | **baseInterface**         | No       |
|                                   | **numMethods**            | No       |
|                                   | **proxyStubClsid32**      | No       |
|                                   | **threadingModel**        | No       |
| **windowClass**                   |                           | No       |
|                                   | **Versionado**             | No       |



 

## <a name="file-location"></a>Ubicación del archivo

Los manifiestos de ensamblado se pueden instalar en tres ubicaciones:

-   Como manifiestos que [acompañan](/windows/desktop/Msi/shared-assemblies)a ensamblados compartidos, los manifiestos de ensamblado deben instalarse como un archivo independiente en la caché de ensamblados en paralelo. Esta suele ser la carpeta WinSxS del Windows directorio.
-   Como manifiestos que acompañan [a ensamblados privados,](/windows/desktop/Msi/private-assemblies)los manifiestos de ensamblado deben instalarse en la estructura de directorios de la aplicación. Normalmente se trata de un archivo independiente en la misma carpeta que el archivo ejecutable de la aplicación.
-   Como recurso de un archivo DLL, el ensamblado está disponible para el uso privado del archivo DLL. Un manifiesto de ensamblado no se puede incluir como un recurso en un archivo EXE. Un archivo EXE puede incluir un [manifiesto de aplicación](application-manifests.md) como un recurso.

## <a name="file-name-syntax"></a>Sintaxis de los nombres de archivo

El nombre de un manifiesto de ensamblado es cualquier nombre de archivo válido seguido de .manifest.

Por ejemplo, un manifiesto de ensamblado que hace referencia a myassembly usaría la siguiente sintaxis de nombre de archivo. Puede omitir el campo <*id.* de recurso> si el manifiesto del ensamblado se está instalando como un archivo independiente o si el identificador de recurso es 1.

<dl> myassembly. <resource ID> . Manifiesto
</dl>

> [!Note]  
> Debido a la forma en que busca ensamblados privados en paralelo, se aplican las siguientes restricciones de nomenclatura al empaquetar un archivo DLL como un ensamblado privado. Una manera recomendada de hacerlo es colocar el manifiesto de ensamblado en el archivo DLL como un recurso. En este caso, el identificador de recurso debe ser igual a 1 y el nombre del ensamblado privado puede ser el mismo que el nombre del archivo DLL. Por ejemplo, si el nombre del archivo DLL es Microsoft.Windows.mysample.dll, el valor del atributo name usado en el elemento **assemblyIdentity** del manifiesto también puede ser Microsoft. Windows.mysample. Una manera alternativa es colocar el manifiesto del ensamblado en un archivo independiente. En este caso, el nombre del ensamblado y su manifiesto deben ser diferentes del nombre del archivo DLL. Por ejemplo, Microsoft. Windows.mysampleAsm, Microsoft. Windows.mysampleAsm.manifest y Microsoft.Windows.Mysample.dll. Para obtener más información sobre cómo busca ensamblados privados en paralelo, vea [Secuencia de búsqueda de ensamblados.](assembly-searching-sequence.md)

 

## <a name="elements"></a>Elementos

Los nombres de elementos y atributos distinguen mayúsculas de minúsculas. Los valores de elementos y atributos no tienen en cuenta las mayúsculas y minúsculas, excepto el valor del atributo type.

<dl> <dt>

<span id="assembly"></span><span id="ASSEMBLY"></span>**ensamblaje**
</dt> <dd>

Elemento contenedor. Su primer subelemento debe ser **un elemento assemblyIdentity** **o noInheritable.** El manifiesto de ensamblado describe de forma única el ensamblado en paralelo identificado por **assemblyIdentity**. Necesario.

El elemento de ensamblado debe estar en el espacio de nombres "urn:schemas-microsoft-com:asm.v1". Los elementos secundarios del ensamblado también deben estar en este espacio de nombres, mediante herencia o etiquetado.

El **elemento** assembly tiene el atributo siguiente.



| Atributo           | Descripción                                           |
|---------------------|-------------------------------------------------------|
| **manifestVersion** | El **atributo manifestVersion** debe establecerse en 1.0. |



 

</dd> <dt>

<span id="noInheritable"></span><span id="noinheritable"></span><span id="NOINHERITABLE"></span>**noInheritable**
</dt> <dd>

Incluya este elemento en un manifiesto de ensamblado para indicar que el ensamblado administra los [contextos de activación](activation-contexts.md) y sus objetos. El **elemento noInheritable** debe ser un subelemento de un **elemento de** ensamblado. El **elemento assemblyIdentity** debe ir después de cualquier **elemento noInheritable.** El **elemento noInheritable** es necesario en el manifiesto del ensamblado si el ensamblado lo usan los [manifiestos](application-manifests.md) de aplicación que incluyen **el elemento noInherit.** Un **elemento noInheritable** en un manifiesto de aplicación no tiene ningún efecto. Un **elemento noInheritable** no tiene elementos secundarios.

</dd> <dt>

<span id="assemblyIdentity"></span><span id="assemblyidentity"></span><span id="ASSEMBLYIDENTITY"></span>**Assemblyidentity**
</dt> <dd>

Describe e identifica de forma única un ensamblado en paralelo.

Como primer subelemento  de un elemento de ensamblado, **assemblyIdentity** describe e identifica de forma única el ensamblado en paralelo propietario de este manifiesto de ensamblado. Esto se denomina ensamblado de contexto **DEFIdentity** del manifiesto del ensamblado.

Como primer subelemento de un elemento **dependentAssembly,** **assemblyIdentity** describe e identifica de forma única un ensamblado en paralelo que usa el ensamblado de contexto DEFIdentity .  Esto se denomina ensamblado de contexto **REFIdentity** del manifiesto del ensamblado. El ensamblado de contexto DEF requiere que el ensamblado ref-context funcione correctamente. Tenga en cuenta que cada ensamblado de contexto **REFIdentity** debe coincidir exactamente con un ensamblado de contexto DEF **correspondienteIdentity** en el propio manifiesto de ensamblado del ensamblado al que se hace referencia.

Este elemento no tiene subelementos. El **elemento assemblyIdentity** tiene los siguientes atributos.



| Atributo                 | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                               |
|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **type**                  | Especifica el tipo de ensamblado. El valor debe ser win32 y en minúsculas. Necesario.                                                                                                                                                                                                                                                                                                                                                         |
| **name**                  | Nombra de forma única el ensamblado. Use el siguiente formato para el nombre del ensamblado: Organization.Division.Name. Por ejemplo, Microsoft. Windows.mysampleAsm. Necesario. Tenga en cuenta que, en el caso de un archivo DLL empaquetado como un ensamblado privado con un archivo de manifiesto independiente, el nombre del ensamblado debe ser diferente del nombre del archivo DLL y del manifiesto.<br/>                                                                              |
| **language**              | Identifica el idioma del ensamblado. Opcional. Si el ensamblado es específico del lenguaje, especifique el código de lenguaje DHTML. En el ensamblado de contexto **DEFIdentity** de un manifiesto de ensamblado destinado a uso en todo el mundo (idioma neutro) omite el atributo language.<br/> En un ensamblado **ref-contextIdentity** de un manifiesto de ensamblado destinado a uso mundial (idioma neutro) establezca el valor de language en " \* ".<br/> |
| **processorArchitecture** | Especifica el procesador. Los valores válidos son x86 para las Windows de 32 bits e ia64 para las Windows de 64 Windows. Opcional.                                                                                                                                                                                                                                                                                                                               |
| **version**               | Especifica la versión del ensamblado. Use el formato de versión de cuatro partes: mmmmm.nnnnn.ooooo.ppppp. Cada una de las partes separadas por puntos puede ser de 0 a 65535, ambos incluidos. Para obtener más información, vea [Versiones de ensamblado.](assembly-versions.md) Necesario.                                                                                                                                                                                               |
| **Publickeytoken**        | Cadena hexadecimal de 16 caracteres que representa los últimos 8 bytes del hash SHA-1 de la clave pública con la que se firma el ensamblado. La clave pública usada para firmar el catálogo debe ser de 2048 bits o superior. Se requiere para los ensamblados en paralelo compartidos.                                                                                                                                                                                |



 

</dd> <dt>

<span id="dependency"></span><span id="DEPENDENCY"></span>**Dependencia**
</dt> <dd>

Elemento contenedor que incluye al menos un **elemento dependentAssembly.** El primer subelemento debe ser un **elemento dependentAssembly.** Una **dependencia** no tiene atributos. Opcional.

</dd> <dt>

<span id="dependentAssembly"></span><span id="dependentassembly"></span><span id="DEPENDENTASSEMBLY"></span>**dependentAssembly**
</dt> <dd>

El primer subelemento debe ser un **elemento assemblyIdentity** que describa e identifique de forma única un ensamblado en paralelo utilizado por el ensamblado en paralelo que posee este manifiesto de ensamblado. Cada **dependentAssembly debe** estar dentro de exactamente una **dependencia**. Opcional.

</dd> <dt>

<span id="file"></span><span id="FILE"></span>**Archivo**
</dt> <dd>

Contiene archivos usados por un ensamblado en paralelo. Contiene **subelementos comClass**, **typelib**, **windowClass**, **comInterfaceProxyStub.** Opcional.

El **elemento** file tiene los atributos siguientes.



| Atributo   | Descripción                                                                                             |
|-------------|---------------------------------------------------------------------------------------------------------|
| **name**    | Nombre del archivo, por ejemplo, Conctl32.dll.                                                            |
| **hashalg** | Algoritmo utilizado para crear un hash del archivo. Este valor debe ser SHA1.                                 |
| **hash**    | Hash del archivo al que se hace referencia por nombre. Cadena hexadecimal de longitud en función del algoritmo hash. |



 

</dd> <dt>

<span id="comClass"></span><span id="comclass"></span><span id="COMCLASS"></span>**comClass**
</dt> <dd>

Subelemento de un **elemento de** archivo. Opcional.

El **elemento comClass** tiene los siguientes atributos.



| Atributo               | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **description**         | Nombre de clase.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| **Clsid**               | GUID que identifica de forma única la clase . Necesario. El valor debe tener el formato de un GUID válido.                                                                                                                                                                                                                                                                                                                                                                                                                             |
| **threadingModel**      | Modelo de subprocesos utilizado por las clases COM en proceso. Si esta propiedad es NULL, no se usa ningún modelo de subprocesos. El componente se crea en el subproceso principal del cliente y las llamadas de otros subprocesos se serializan a este subproceso. Opcional. Los valores válidos son: "Apartment", "Free", "Both" y "Neutral".                                                                                                                                                                                                                         |
| **tlbid**               | GUID de la biblioteca de tipos para este componente COM. El valor debe tener el formato de un GUID. Opcional.                                                                                                                                                                                                                                                                                                                                                                                                                              |
| **Progid**              | Identificador de programación dependiente de la versión asociado al componente COM. El formato de un ProgID se <*proveedor>.<* componente *>.<* versión *>.*                                                                                                                                                                                                                                                                                                                                                                      |
| **miscStatus**          | Duplica en el manifiesto del ensamblado la información proporcionada por la clave del Registro MiscStatus. Si no se encuentran valores para los atributos **miscStatusIcon**, **miscStatusContent**, **miscStatusDocprint** o **miscStatusThumbnail,** se usa el valor predeterminado correspondiente que aparece en **miscStatus** para los atributos que faltan. El valor puede ser una lista delimitada por comas de los valores de atributo de la tabla siguiente. Puede usar este atributo si la clase COM es una clase OCX que requiere valores de clave del Registro Miscstatus. |
| **miscStatusIcon**      | Duplica en el manifiesto del ensamblado la información proporcionada por DVASPECT \_ ICON. Puede proporcionar un icono de un objeto . El valor puede ser una lista delimitada por comas de los valores de atributo de la tabla siguiente. Puede usar este atributo si la clase COM es una clase OCX que requiere valores de clave del Registro Miscstatus.                                                                                                                                                                                                                |
| **miscStatusContent**   | Duplica en el manifiesto del ensamblado la información proporcionada por DVASPECT \_ CONTENT. Puede proporcionar un documento compuesto que se puede mostrar para una pantalla o impresora. El valor puede ser una lista delimitada por comas de los valores de atributo de la tabla siguiente. Puede usar este atributo si la clase COM es una clase OCX que requiere valores de clave del Registro Miscstatus.                                                                                                                                                                          |
| **miscStatusDocprint**  | Duplica en el manifiesto del ensamblado la información proporcionada por DVASPECT \_ DOCPRINT. Puede proporcionar una representación de objeto que se puede mostrar en la pantalla como si se imprimira en una impresora. El valor puede ser una lista delimitada por comas de los valores de atributo de la tabla siguiente. Puede usar este atributo si la clase COM es una clase OCX que requiere valores de clave del Registro Miscstatus.                                                                                                                                               |
| **miscStatusThumbnail** | Duplica en un manifiesto de ensamblado la información proporcionada por DVASPECT \_ THUMBNAIL. Puede proporcionar una miniatura de un objeto que se puede mostrar en una herramienta de exploración. El valor puede ser una lista delimitada por comas de los valores de atributo de la tabla siguiente. Puede usar este atributo si la clase COM es una clase OCX que requiere valores de clave del Registro Miscstatus.                                                                                                                                                                         |



 

El **elemento comClass** puede tener elementos progid ... como elementos &lt; &gt; </progid> secundarios, que enumera los progids dependientes de la versión.

En el ejemplo siguiente se muestra **un elemento comClass** incluido en un **elemento de** archivo.

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

Si la clase COM es una clase OCX que requiere la subclave del Registro MiscStatus para especificar cómo crear y mostrar un objeto, puede habilitar el objeto duplicando esta información en el manifiesto del ensamblado. Especifique las características del objeto mediante los atributos **miscStatus**, **miscStatusIcon**, **miscStatusContent**, **miscStatusDocprint y** **miscStatusThumbnail** del elemento **comClass.** Establezca estos atributos en una lista separada por comas de valores de atributo de la tabla siguiente. Estos atributos duplican la información que proporcionaría una enumeración DVASPECT. Si no se encuentra ningún valor para **miscStatusIcon,** **miscStatusContent**, **miscStatusDocprint** o **miscStatusThumbnail**, se usan los valores predeterminados especificados en **miscStatus.** Use valores de atributo de la tabla siguiente. Corresponden a las marcas de bits de una [**enumeración OLEMISC.**](/windows/win32/api/oleidl/ne-oleidl-olemisc)



| Valor del atributo              | Constante OLEMISC                      |
|------------------------------|---------------------------------------|
| rempomposeonresize            | REMPOMPOSEONRESIZE DE OLEMISC \_            |
| onlyiconic                   | OLEMISC \_ ONLYICONIC                   |
| insertnotreplace             | OLEMISC \_ INSERTNOTREPLACE             |
| static                       | OLEMISC \_ STATIC                       |
| cantlink reenlace               | OLEMISC \_ CANTLINK REENLACE               |
| canlinkbyole1                | OLEMISC \_ CANLINKBYOLE1                |
| islinkobject                 | OLEMISC \_ ISLINKOBJECT                 |
| Insideout                    | OLEMISC \_ INSIDEOUT                    |
| activatewhenvisible          | OLEMISC \_ ACTIVATEWHENVISIBLE          |
| renderingisdeviceindependent | OLEMISC \_ RENDERINGISDEVICEINDEPENDENT |
| invisibleatruntime           | OLEMISC \_ INVISIBLEATRUNTIME           |
| alwaysrun                    | OLEMISC \_ ALWAYSRUN                    |
| actslikebutton               | OLEMISC \_ ACTSLIKEBUTTON               |
| actslikelabel                | OLEMISC \_ ACTSLIKELABEL                |
| nouiactivate                 | OLEMISC \_ NOUIACTIVATE                 |
| alineable                    | OLEMISC \_ ALIGNABLE                    |
| simpleframe                  | OLEMISC \_ SIMPLEFRAME                  |
| setclientsitefirst           | OLEMISC \_ SETCLIENTSITEFIRST           |
| Imemode                      | TOLEMISC \_ IMEMODE                     |
| ignoreativatewhenvisible     | OLEMISC \_ IGNOREACTIVATEWHENVISIBLE    |
| wantstomenumerge             | OLEMISC \_ WANTSTOMENUMERGE             |
| supportsmultilevelundo       | OLEMISC \_ SUPPORTSMULTILEVELUNDO       |



 

</dd> <dt>

<span id="typelib"></span><span id="TYPELIB"></span>**Typelib**
</dt> <dd>

Subelemento de un **elemento de** archivo. Opcional.

El **elemento typelib** tiene los atributos que se muestran en la tabla siguiente.



| Atributo      | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                     |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **tlbid**      | Identificador único de la biblioteca de tipos. Necesario.                                                                                                                                                                                                                                                                                                                                                                                    |
| **version**    | Número de versión de dos partes de la biblioteca de tipos. Si solo aumenta el número de versión secundaria, todas las características de la biblioteca de tipos anterior se admiten de una manera compatible. Si cambia el número de versión principal, se debe volver a compilar el código compilado con la biblioteca de tipos. El número de versión de la biblioteca de tipos puede diferir del número de versión de la aplicación. Necesario.                                      |
| **helpdir**    | Directorio donde se encuentra el archivo de Ayuda para los tipos de la biblioteca de tipos. Si la aplicación admite bibliotecas de tipos para varios lenguajes, las bibliotecas pueden hacer referencia a nombres de archivo diferentes en el directorio de archivos de Ayuda. Si no hay ningún valor, especifique "". Necesario.                                                                                                                                                          |
| **resourceid** | Representación de cadena hexadecimal del identificador de configuración regional (LCID). Es de uno a cuatro dígitos hexadecimales sin prefijo 0x y sin ceros a la izquierda. El LCID puede tener un identificador de subidioma neutro. Para obtener más información, vea [Identificadores de configuración regional.](/windows/desktop/Intl/locale-identifiers) Opcional.                                                                                                                                      |
| **flags**      | Representación de cadena de las marcas de la biblioteca de tipos para esta biblioteca de tipos. En concreto, debe ser "RESTRICTED", "CONTROL", "HIDDEN" y "HASDISKIMAGE". Estos son los valores de la enumeración [**LIBFLAGS**](/windows/win32/api/oaidl/ne-oaidl-libflags) y son las mismas marcas especificadas en el parámetro *uLibFlags* del método [**ICreateTypeLib::SetLibFlags.**](/windows/win32/api/oaidl/nf-oaidl-icreatetypelib-setlibflags) Opcional. |



 

En el ejemplo siguiente se muestra **un elemento typelib** incluido en un **elemento de** archivo.

``` syntax
<file name="sampleu.dll">
       <typelib tlbid="{44EC0535-400F-11D0-9DCD-00A0C90391D3}"
       version="1.0" helpdir=""/>
</file>
```

</dd> <dt>

<span id="comInterfaceExternalProxyStub"></span><span id="cominterfaceexternalproxystub"></span><span id="COMINTERFACEEXTERNALPROXYSTUB"></span>**comInterfaceExternalProxyStub**
</dt> <dd>

**comInterfaceExternalProxyStub** es un subelemento de un elemento **de** ensamblado y se usa para interfaces de automatización. Por ejemplo, [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) y sus interfaces derivadas. Opcional.

La implementación predeterminada del código auxiliar de proxy es adecuada para la mayoría de las interfaces de automatización, como las interfaces derivadas de [**IDispatch.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) El código auxiliar del proxy de interfaz y todas las demás implementaciones de interfaz de código auxiliar de proxy externo deben aparecer en **comInterfaceExternalProxyStub**. El **elemento comInterfaceExternalProxyStub** tiene los atributos que se muestran en la tabla siguiente.



| Atributo         | Descripción                                                                                                                                                                                 |
|-------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Iid**           | El IID de la interfaz para la que se declara el proxy. Necesario. El valor debe tener el formato: "{iid}".                                                                         |
| **baseInterface** | El IID de la interfaz de la que se deriva el descrito por el atributo **iid.** Este atributo es opcional. El valor debe tener el formato: "{iid}".                            |
| **numMethods**    | Número de métodos implementados por la interfaz . Este atributo es opcional. El valor debe tener el formato: "n".                                                                       |
| **name**          | Nombre de la interfaz tal como aparecería en el código. Por ejemplo, "IViewObject". No debe ser una cadena descriptiva. Este atributo es opcional. El valor debe tener el formato: "name". |
| **tlbid**         | Biblioteca de tipos que contiene la descripción de la interfaz especificada por el **atributo iid.** Este atributo es opcional. El valor debe tener el formato: "{tlbid}".                |
| proxyStubClsid32  | Mapas un IID a un CLSID en archivos DLL de proxy de 32 bits.                                                                                                                                                |



 

En el ejemplo siguiente se **muestra un elemento comInterfaceExternalProxyStub.**

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

Subelemento de un **elemento de** archivo. Opcional.

Si un archivo del ensamblado implementa un código auxiliar de proxy, la etiqueta de archivo correspondiente debe incluir un subelemento **comInterfaceProxyStub** que tenga atributos idénticos a un **elemento comInterfaceProxyStub.** Es posible que las interfaces de serialización entre procesos y subprocesos no funcionen según lo previsto si omite algunas de las dependencias **comInterfaceProxyStub** para el componente.

El **elemento comInterfaceProxyStub** tiene los siguientes atributos.



| Atributo            | Descripción                                                                                                                                                                                                                                                                                                 |
|----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Iid**              | El. IID de la interfaz para la que se declara el proxy. Necesario. El valor debe tener el formato: "{iid}".                                                                                                                                                                                        |
| **name**             | Nombre de la interfaz tal como aparecería en el código. Por ejemplo, "IViewObject". No debe ser una cadena descriptiva. Este atributo es opcional. El valor debe tener el formato: "name".                                                                                                                 |
| **tlbid**            | Biblioteca de tipos que contiene la descripción de la interfaz especificada por el **atributo iid.** Este atributo es opcional. El valor debe tener el formato: "{tlbid}".                                                                                                                                 |
| **baseInterface**    | El IID de la interfaz de la que se deriva el descrito por el atributo **iid.** Este atributo es opcional. El valor debe tener el formato: "{iid}".                                                                                                                                            |
| **numMethods**       | Número de métodos implementados por la interfaz . Este atributo es opcional. El valor debe tener el formato: "n".                                                                                                                                                                                       |
| **proxyStubClsid32** | Mapas un IID a un CLSID en archivos DLL de proxy de 32 bits.                                                                                                                                                                                                                                                                |
| **threadingModel**   | Modelo de subprocesos utilizado por las clases COM en proceso. Si esta propiedad es NULL, no se usa ningún modelo de subprocesos. El componente se crea en el subproceso principal del cliente y las llamadas de otros subprocesos se serializan a este subproceso. Opcional. Los valores válidos son: "Apartment", "Free", "Both" y "Neutral". |



 

</dd> <dt>

<span id="windowclass"></span><span id="WINDOWCLASS"></span>**windowclass**
</dt> <dd>

Nombre de una clase de Windows de la que se va a crear una versión. El **elemento windowclass** tiene el atributo siguiente.



| Atributo     | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Versionado** | Este atributo controla si el nombre de clase de ventana interno usado en el registro contiene la versión del ensamblado que contiene la clase de ventana. El valor de este atributo puede ser "yes" o "no". El valor predeterminado es "yes". El valor "no" solo debe usarse si un componente en paralelo y un componente equivalente no en paralelo definen la misma clase de ventana y desea tratarlos como la misma clase de ventana. Tenga en cuenta que las reglas habituales sobre el registro de clases de ventana solo se aplican al primer componente que registra la clase de ventana, ya que no tiene versiones. |



 

En el ejemplo siguiente se muestra **un elemento windowclass** incluido en un **elemento de** archivo.

``` syntax
<file name="comctl32.dll">
        <windowClass versioned="no">ToolbarWindow32</windowClass>
</file>
```

</dd> </dl>

## <a name="example"></a>Ejemplo

A continuación se muestra un ejemplo de un manifiesto de ensamblado.

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

 

