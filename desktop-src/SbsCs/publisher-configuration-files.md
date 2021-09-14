---
description: Un archivo de configuración del publicador es un archivo XML que redirige globalmente las aplicaciones y ensamblados del uso de una versión de un ensamblado en paralelo a otra versión del mismo ensamblado.
ms.assetid: b10752af-80a7-4027-b525-90333d0d010a
title: Publisher Archivos de configuración
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4cc5d7d7b7ffdad3d1179a7f8c66a347d91e0a03
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071337"
---
# <a name="publisher-configuration-files"></a>Publisher Archivos de configuración

Un archivo de configuración del publicador es un archivo XML que redirige globalmente las aplicaciones y ensamblados del uso de una versión de un ensamblado en paralelo a otra versión del mismo ensamblado. Normalmente, el publicador del ensamblado emite una actualización compatible o una corrección de seguridad por ensamblado mediante la emisión de un archivo de configuración del publicador que se instalará junto con una actualización de Service Pack. Esto se conoce como configuración [del publicador.](publisher-configuration.md) Para obtener más información sobre este tipo de [configuración,](configuration.md) vea Publisher Configuration.

Publisher archivos de configuración tienen los siguientes elementos y atributos. Para obtener una lista completa del esquema XML, [vea Publisher de archivo de configuración .](publisher-configuration-file-schema.md)



| Elemento               | Atributos                | Obligatorio |
|-----------------------|---------------------------|----------|
| **ensamblaje**          |                           | Sí      |
|                       | **manifestVersion**       | Sí      |
| **Assemblyidentity**  |                           | Sí      |
|                       | **type**                  | Sí      |
|                       | **name**                  | Sí      |
|                       | **language**              | No       |
|                       | **processorArchitecture** | No       |
|                       | **version**               | Sí      |
|                       | **Publickeytoken**        | No       |
| **Dependencia**        |                           | No       |
| **dependentAssembly** |                           | No       |
| **bindingRedirect**   |                           | Sí      |
|                       | **oldVersion**            | Sí      |
|                       | **newVersion**            | Sí      |



 

## <a name="file-location"></a>Ubicación del archivo

Publisher archivos de configuración deben instalarse en la carpeta WinSxS. Normalmente se instalan como un archivo independiente, pero los archivos de configuración del publicador también se pueden incluir como un recurso en un archivo DLL. Un archivo de configuración del publicador no se puede incluir como un recurso en un archivo EXE. Un archivo EXE puede incluir un [manifiesto de aplicación](application-manifests.md) como recurso.

## <a name="file-name-syntax"></a>Sintaxis de los nombres de archivo

El nombre de archivo de un archivo de configuración del publicador tiene la directiva de *formulario*. *principal.* *secundaria.* *assemblyname* donde *principal* y *secundaria* hacen referencia a las partes principales y secundarias de la versión [del ensamblado](assembly-versions.md) que se ve afectada. Assemblyname *hace* referencia al nombre del ensamblado.

Por ejemplo, un archivo de configuración del publicador para la versión 6.0 de Microsoft. Windows. El ensamblado Common-Controls tendría el nombre siguiente:

<dl> policy.6.0.Microsoft. Windows. Common-Controls  
</dl>

No use archivos de configuración de directiva para incrementar la versión principal o secundaria de un ensamblado. Por ejemplo, no redirija la versión 6.0.0.0 a 7.0.0.0 o 6.1.0.0. Cuando una aplicación hace referencia a una versión de ensamblado, como 6.0.0.0, comprueba en paralelo la presencia de cualquier archivo de configuración de directiva con las versiones principales y secundarias especificadas, por ejemplo, 6.0. A continuación, la aplicación se redirige a otra versión del ensamblado, por ejemplo, 6.0.1.0. Si un archivo de configuración del publicador incrementa la versión principal o secundaria de un ensamblado, el redireccionamiento posterior del ensamblado puede requerir la emisión de varios archivos de configuración de directiva.

## <a name="elements"></a>Elementos

<dl> <dt>

<span id="assembly"></span><span id="ASSEMBLY"></span>**ensamblaje**
</dt> <dd>

Elemento contenedor. Su primer subelemento debe ser **assemblyIdentity.** Necesario.

El elemento assembly debe estar en el espacio de nombres **urn:schemas-microsoft-com:asm.v1**. Los elementos secundarios del ensamblado también deben estar en este espacio de nombres, por herencia o etiquetado.

El **elemento** de ensamblado tiene los siguientes atributos.



| Atributo           | Descripción                                           |
|---------------------|-------------------------------------------------------|
| **manifestVersion** | El **atributo manifestVersion** debe establecerse en 1.0. |



 

</dd> <dt>

<span id="assemblyIdentity"></span><span id="assemblyidentity"></span><span id="ASSEMBLYIDENTITY"></span>**Assemblyidentity**
</dt> <dd>

Describe e identifica de forma única un ensamblado en paralelo.

Como primer subelemento  de un elemento de ensamblado, **assemblyIdentity** describe el ensamblado en paralelo que tiene una o varias de sus dependencias de ensamblado modificadas. El archivo de configuración del publicador redirige las dependencias del ensamblado identificado. Por ejemplo, el siguiente **assemblyIdentity** indica que el archivo de configuración del publicador afecta a las dependencias de Microsoft x86. Windows. Ensamblado pop 6.0.0.0.

``` syntax
<assemblyIdentity 
     type="win32-policy" 
     publicKeyToken="0000000000000000" 
     name="policy.6.0.Microsoft.Windows.Pop" 
     version="2.1.0.0" 
     processorArchitecture="x86"/>
```

Como primer subelemento de un **elemento dependentAssembly,** **assemblyIdentity** describe una dependencia de ensamblado en paralelo. El archivo de configuración del publicador vuelve a configurar la identidad de este ensamblado en paralelo necesario. El cambio se especifica en **bindingRedirect.** Por ejemplo, el ensamblado **siguienteIdentity cambia** cualquier dependencia de Microsoft. Windows. SampleAssembly versión 2.0.0.0 para una dependencia de Microsoft. Windows. SampleAssembly versión 2.0.1.0.

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

El **elemento assemblyIdentity** tiene los atributos siguientes. No tiene elementos secundarios.



| Atributo                 | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|---------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **type**                  | Especifica el tipo de ensamblado. Necesario. En **assemblyIdentity para** el ensamblado que se ve afectado, el valor del atributo **de** tipo debe establecerse en win32-policy. El valor win32-policy debe estar en minúsculas.<br/> En **assemblyIdentity para la** dependencia de ensamblado cambiante, el valor del atributo **de** tipo debe establecerse en win32. El valor win32 debe estar en minúsculas.<br/>                                                                                                                                                                                                             |
| **name**                  | Nombra de forma única un ensamblado. Necesario. En **assemblyIdentity para** el ensamblado afectado, name tiene la directiva de *formulario*. *principal.* *secundaria.* *assemblyname donde* *principal* y *secundaria* hacen referencia a las partes principales y secundarias de la versión [del ensamblado](assembly-versions.md).<br/> En **assemblyIdentity para la** dependencia de ensamblado cambiante, el nombre tiene el formato Organization.Division.Name. Por ejemplo, Microsoft. Windows. MysampleApp.<br/>                                                                                                                                                                                 |
| **language**              | Identifica el idioma del ensamblado. Opcional. En **assemblyIdentity para** el ensamblado que se ve afectado, si el ensamblado es específico del lenguaje, especifique el código de lenguaje DHTML. Si el ensamblado es para uso internacional (idioma neutro), omita este atributo.<br/> En **assemblyIdentity para la** dependencia de ensamblado cambiante, si el ensamblado es específico del lenguaje, especifique el código de lenguaje DHTML. Si el ensamblado es para uso internacional (idioma neutro) establezca el valor en " \* ".<br/>                                                                                                                            |
| **processorArchitecture** | Especifica el procesador que ejecuta la aplicación.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| **version**               | Especifica la versión del ensamblado. Usar sintaxis de versión de cuatro partes: mmmm.nnnn.oooo.pppp Solo se requiere en el ensamblado de contexto **DEFIdentity**. No especifique el atributo version en el ensamblado **ref-contextIdentity**.                                                                                                                                                                                                                                                                                                                                                                                                                        |
| **Publickeytoken**        | Cadena hexadecimal de 16 caracteres que representa los últimos 8 bytes del hash SHA-1 de la clave pública con la que se firma el ensamblado. La clave pública que se usa para firmar el catálogo debe ser de 2048 bits o superior. Se requiere un publicKeyToken para todos los ensamblados en paralelo compartidos. PublicKeyToken usado para el archivo de configuración del publicador debe ser la misma clave que se usa para el ensamblado firmado. Publisher archivos de configuración se pueden firmar con las mismas [](assembly-signing-example.md) herramientas que se usan con ensamblados, vea Ejemplo de firma de ensamblados y Creación de archivos [y catálogos firmados.](creating-signed-files-and-catalogs.md) |



 

</dd> <dt>

<span id="dependency"></span><span id="DEPENDENCY"></span>**Dependencia**
</dt> <dd>

Un elemento contenedor opcional para al menos **un elemento dependentAssembly**. No tiene atributos.

</dd> <dt>

<span id="dependentAssembly"></span><span id="dependentassembly"></span><span id="DEPENDENTASSEMBLY"></span>**dependentAssembly**
</dt> <dd>

Cada **dependentAssembly debe** estar dentro de exactamente una **dependencia**. **DependentAssembly** no tiene atributos. El primer subelemento de **dependentAssembly** debe ser **assemblyIdentity** para el ensamblado en paralelo que se va a volver a configurar mediante la configuración del publicador.

</dd> <dt>

<span id="bindingRedirect"></span><span id="bindingredirect"></span><span id="BINDINGREDIRECT"></span>**bindingRedirect**
</dt> <dd>

El **elemento bindingRedirect** contiene información de redirección para el enlace del ensamblado.

Este elemento tiene los atributos que se muestran en la tabla siguiente.



| Atributo      | Descripción                                                                                                                                                                                                                           |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **oldVersion** | Especifica la versión del ensamblado que se va a invalidar y redirigir. Use la sintaxis de versión de cuatro partes nnnnn.nnnnn.nnnnn.nnnnn. Especifique un intervalo de versiones mediante un guion sin espacios. Por ejemplo, 2.14.3.0 o 2.14.3.0 2.16.0.0. Necesario. |
| **newVersion** | Especifica la versión del ensamblado de reemplazo. Use la sintaxis de versión de cuatro partes nnnnn.nnnnn.nnnnn.nnnnn.                                                                                                                                     |



 

</dd> </dl>

## <a name="remarks"></a>Observaciones

Publisher archivos de configuración no especifican archivos. Tenga en cuenta que los archivos de directiva específicos del lenguaje son independientes del archivo de configuración del publicador.

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

 

 




