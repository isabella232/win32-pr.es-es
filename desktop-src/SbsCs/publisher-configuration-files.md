---
description: Un archivo de configuración de publicador es un archivo XML que redirige globalmente las aplicaciones y los ensamblados con una versión de un ensamblado en paralelo a otra versión del mismo ensamblado.
ms.assetid: b10752af-80a7-4027-b525-90333d0d010a
title: Archivos de configuración del publicador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4cc5d7d7b7ffdad3d1179a7f8c66a347d91e0a03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912506"
---
# <a name="publisher-configuration-files"></a>Archivos de configuración del publicador

Un archivo de configuración de publicador es un archivo XML que redirige globalmente las aplicaciones y los ensamblados con una versión de un ensamblado en paralelo a otra versión del mismo ensamblado. Normalmente, el publicador del ensamblado emite una corrección de seguridad o actualización compatible en cada ensamblado mediante la emisión de un archivo de configuración del publicador que se va a instalar junto con una actualización Service Pack. Esto se conoce como [configuración del publicador](publisher-configuration.md). Para obtener más información acerca de este tipo de [configuración](configuration.md) , consulte Configuración del publicador.

Los archivos de configuración del publicador tienen los siguientes elementos y atributos. Para obtener una lista completa del esquema XML, vea [esquema del archivo de configuración del publicador](publisher-configuration-file-schema.md).



| Elemento               | Atributos                | Obligatorio |
|-----------------------|---------------------------|----------|
| **assembl**          |                           | Sí      |
|                       | **manifestVersion**       | Sí      |
| **assemblyIdentity**  |                           | Sí      |
|                       | **type**                  | Sí      |
|                       | **name**                  | Sí      |
|                       | **language**              | No       |
|                       | **processorArchitecture** | No       |
|                       | **version**               | Sí      |
|                       | **publicKeyToken**        | No       |
| **pendiente**        |                           | No       |
| **dependentAssembly** |                           | No       |
| **bindingRedirect**   |                           | Sí      |
|                       | **oldVersion**            | Sí      |
|                       | **newVersion**            | Sí      |



 

## <a name="file-location"></a>Ubicación del archivo

Los archivos de configuración del publicador deben instalarse en la carpeta WinSxS. Normalmente se instalan como un archivo independiente, pero los archivos de configuración del publicador también se pueden incluir como un recurso en un archivo DLL. Un archivo de configuración de publicador no se puede incluir como un recurso en un archivo EXE. Un archivo EXE puede incluir un [manifiesto de aplicación](application-manifests.md) como un recurso.

## <a name="file-name-syntax"></a>Sintaxis de los nombres de archivo

El nombre de archivo de un archivo de configuración de publicador tiene la *Directiva* de formulario. *principal*. *secundaria*. *AssemblyName* , donde *major* y *Minor* hacen referencia a las partes principales y secundarias de la [versión de ensamblado](assembly-versions.md) que se va a ver afectada. *AssemblyName* hace referencia al nombre del ensamblado.

Por ejemplo, un archivo de configuración de publicador para la versión 6,0 del ensamblado Microsoft. Windows. Common-Controls tendría el siguiente nombre:

<dl> Policy. 6.0. Microsoft. Windows. Common-Controls  
</dl>

No use archivos de configuración de directivas para incrementar la versión principal o secundaria de un ensamblado. Por ejemplo, no redirija la versión 6.0.0.0 a 7.0.0.0 o 6.1.0.0. Cuando una aplicación hace referencia a una versión de ensamblado, como 6.0.0.0, comprueba la presencia de cualquier archivo de configuración de directiva con las versiones principal y secundaria especificadas, por ejemplo, 6,0. A continuación, la aplicación se redirige a otra versión del ensamblado, por ejemplo 6.0.1.0. Si un archivo de configuración del publicador incrementa la versión principal o secundaria de un ensamblado, la redirección posterior del ensamblado puede requerir la emisión de varios archivos de configuración de directivas.

## <a name="elements"></a>Elementos

<dl> <dt>

<span id="assembly"></span><span id="ASSEMBLY"></span>**assembl**
</dt> <dd>

Elemento contenedor. Su primer subelemento debe ser **assemblyIdentity**. Obligatorio.

El elemento de ensamblado debe estar en el espacio de nombres **urn: schemas-microsoft-com: ASM. v1**. Los elementos secundarios del ensamblado también deben estar en este espacio de nombres, por herencia o mediante el etiquetado.

El elemento **Assembly** tiene los atributos siguientes.



| Atributo           | Descripción                                           |
|---------------------|-------------------------------------------------------|
| **manifestVersion** | El atributo **manifestVersion** debe establecerse en 1,0. |



 

</dd> <dt>

<span id="assemblyIdentity"></span><span id="assemblyidentity"></span><span id="ASSEMBLYIDENTITY"></span>**assemblyIdentity**
</dt> <dd>

Describe e identifica de forma única un ensamblado en paralelo.

Como primer subelemento de un elemento **Assembly** , **assemblyIdentity** describe el ensamblado en paralelo que tiene una o varias de sus dependencias de ensamblado cambiadas. El archivo de configuración del publicador redirige las dependencias del ensamblado identificado. Por ejemplo, el siguiente **assemblyIdentity** indica que el archivo de configuración del publicador afecta a las dependencias del ensamblado de 6.0.0.0 x86 Microsoft. Windows. pop.

``` syntax
<assemblyIdentity 
     type="win32-policy" 
     publicKeyToken="0000000000000000" 
     name="policy.6.0.Microsoft.Windows.Pop" 
     version="2.1.0.0" 
     processorArchitecture="x86"/>
```

Como primer subelemento de un elemento **dependentAssembly** , **assemblyIdentity** describe una dependencia del ensamblado en paralelo. El archivo de configuración del publicador vuelve a configurar la identidad de este ensamblado en paralelo necesario. El cambio se especifica en un **bindingRedirect**. Por ejemplo, el siguiente **assemblyIdentity** cambia cualquier dependencia de la versión 2.0.0.0 de Microsoft. Windows. SampleAssembly a una dependencia de la versión de Microsoft. Windows. SampleAssembly 2.0.1.0.

``` syntax
<dependency>
      <dependentAssembly>
         <assemblyIdentity 
type="win32" 
name="Microsoft.Windows.SampleAssembly"  
processorArchitecture="x86"
publicKeyToken="0000000000000000"/>
         <bindingRedirect oldVersion="2.0.0.0" newVersion="2.0.1.0"/>
      </dependentAssembly>
</dependency>
```

El elemento **assemblyIdentity** tiene los atributos siguientes. No tiene subelementos.



| Atributo                 | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|---------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **type**                  | Especifica el tipo de ensamblado. Obligatorio. En el **assemblyIdentity** para que el ensamblado se vea afectado, el valor del atributo **Type** debe establecerse en Win32-Policy. El valor Win32-Policy debe estar en minúsculas.<br/> En el **assemblyIdentity** para la dependencia del ensamblado cambiante, el valor del atributo **Type** debe establecerse en Win32. El valor Win32 debe estar en minúsculas.<br/>                                                                                                                                                                                                             |
| **name**                  | Designa de forma única un ensamblado. Obligatorio. En el **assemblyIdentity** para que el ensamblado se vea afectado, el nombre tiene la *Directiva* de formulario. *principal*. *secundaria*. *AssemblyName* donde *major* y *Minor* hacen referencia a las partes principales y secundarias de la [versión del ensamblado](assembly-versions.md).<br/> En el **assemblyIdentity** para la dependencia del ensamblado cambiante, Name tiene el formato Organization.Division.Name. Por ejemplo, Microsoft. Windows. MysampleApp.<br/>                                                                                                                                                                                 |
| **language**              | Identifica el idioma del ensamblado. Opcional. En el **assemblyIdentity** para que el ensamblado se vea afectado, si el ensamblado es específico del idioma, especifique el código de lenguaje DHTML. Si el ensamblado es para uso internacional (idioma neutro), omita este atributo.<br/> En el **assemblyIdentity** para la dependencia del ensamblado cambiante, si el ensamblado es específico del idioma, especifique el código de lenguaje DHTML. Si el ensamblado es para uso internacional (idioma neutro), establezca el valor como " \* ".<br/>                                                                                                                            |
| **processorArchitecture** | Especifica el procesador que ejecuta la aplicación.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| **version**               | Especifica la versión del ensamblado. Use la sintaxis de versión de cuatro partes: mmmm. nnnn. oooo. pppp Solo se requiere en el **assemblyIdentity** de Def-context. No especifique el atributo de versión en el **assemblyIdentity** de referencia.                                                                                                                                                                                                                                                                                                                                                                                                                        |
| **publicKeyToken**        | Cadena hexadecimal de 16 caracteres que representa los últimos 8 bytes del hash SHA-1 de la clave pública con la que se firma el ensamblado. La clave pública que se usa para firmar el catálogo debe ser de 2048 bits o superior. Se requiere un publicKeyToken para todos los ensamblados en paralelo compartidos. El publicKeyToken utilizado para el archivo de configuración del publicador debe ser la misma clave utilizada para el ensamblado firmado. Los archivos de configuración del publicador se pueden firmar con las mismas herramientas que se usan con los ensamblados, vea [ejemplo de firma de ensamblados](assembly-signing-example.md) y [crear archivos y catálogos firmados](creating-signed-files-and-catalogs.md). |



 

</dd> <dt>

<span id="dependency"></span><span id="DEPENDENCY"></span>**pendiente**
</dt> <dd>

Un elemento contenedor opcional para al menos un elemento **dependentAssembly**. No tiene atributos.

</dd> <dt>

<span id="dependentAssembly"></span><span id="dependentassembly"></span><span id="DEPENDENTASSEMBLY"></span>**dependentAssembly**
</dt> <dd>

Cada **dependentAssembly** debe estar dentro de una **dependencia** exactamente. Un **dependentAssembly** no tiene atributos. El primer subelemento de **dependentAssembly** debe ser un **assemblyIdentity** para que la configuración del publicador reconfigure el ensamblado en paralelo.

</dd> <dt>

<span id="bindingRedirect"></span><span id="bindingredirect"></span><span id="BINDINGREDIRECT"></span>**bindingRedirect**
</dt> <dd>

El elemento **bindingRedirect** contiene información de redirección para el enlace del ensamblado.

Este elemento tiene los atributos que se muestran en la tabla siguiente.



| Atributo      | Descripción                                                                                                                                                                                                                           |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **oldVersion** | Especifica la versión de ensamblado que se va a reemplazar y redirigir. Use la sintaxis de la versión de cuatro partes nnnnn. nnnnn. nnnnn. nnnnn. Especifique un intervalo de versiones por un guión sin espacios. Por ejemplo, 2.14.3.0 o 2.14.3.0 2.16.0.0. Obligatorio. |
| **newVersion** | Especifica la versión del ensamblado de reemplazo. Use la sintaxis de versión de cuatro partes nnnnn. nnnnn. nnnnn. nnnnn.                                                                                                                                     |



 

</dd> </dl>

## <a name="remarks"></a>Observaciones

Los archivos de configuración del publicador no especifican archivos. Tenga en cuenta que los archivos de directivas específicos del idioma son independientes del archivo de configuración del publicador.

## <a name="example"></a>Ejemplo

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
<assemblyIdentity type="win32-policy" publicKeyToken="0000000000000000" name="policy.6.0.Proseware.Research.SampleAssembly" version="1.0.1.0" language="en-us" processorArchitecture="x86"/>
<dependency>
<dependentAssembly>
<assemblyIdentity type="win32" publicKeyToken="0000000000000000" name="Proseware.Research.SampleAssembly" language="en-us" processorArchitecture="x86"/>
<bindingRedirect oldVersion="1.0.0.0" newVersion="1.0.1.0"/>
</dependentAssembly>
</dependency>
</assembly>
```

 

 




