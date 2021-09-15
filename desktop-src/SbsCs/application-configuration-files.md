---
description: Un archivo de configuración de aplicación es un archivo XML que se usa para controlar el enlace de ensamblados.
ms.assetid: b7453f2b-52a4-4af9-8410-ebbb430ada67
title: Archivos de configuración de la aplicación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b1a2e0f6b493c217aded9e11507f660d517b400
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127271759"
---
# <a name="application-configuration-files"></a>Archivos de configuración de la aplicación

Un archivo de configuración de aplicación es un archivo XML que se usa para controlar el enlace de ensamblados. Puede redirigir una aplicación desde el uso de una versión de un ensamblado en paralelo a otra versión del mismo ensamblado. Esto se denomina [configuración por aplicación.](per-application-configuration.md) Un archivo de configuración de aplicación solo se aplica a un manifiesto de aplicación específico y ensamblados dependientes. Los componentes aislados compilados con un manifiesto de id. de recurso de MANIFIESTO ISOLATIONAWARE incrustado \_ requieren un archivo de configuración de aplicación \_ \_ independiente. Los manifiestos administrados [**con CreateActCtx**](/windows/desktop/api/Winbase/nf-winbase-createactctxa) requieren un archivo de configuración de aplicación independiente.

El redireccionamiento especificado por un archivo de configuración de aplicación puede invalidar las versiones de ensamblado especificadas por los [manifiestos de](application-manifests.md) aplicación y los archivos [de configuración del publicador](publisher-configuration-files.md). Por ejemplo, si un archivo de configuración del publicador especifica que todas las referencias a un ensamblado se redirijan de la versión 1.0.0.0 a la 1.1.0.0, se puede usar un archivo de configuración de la aplicación para redirigir una aplicación determinada para que use la versión 1.0.0.0. Un archivo de configuración de aplicación solo se aplica al manifiesto de aplicación especificado y a los ensamblados dependientes.

Para obtener una lista completa del esquema XML, vea [Esquema del archivo de configuración de la aplicación.](application-configuration-file-schema.md)

Los archivos de configuración de la aplicación tienen los elementos y atributos que se muestran en la tabla siguiente.



| Elemento               | Atributos                | Requerido |
|-----------------------|---------------------------|----------|
| **configuration**     |                           | Sí      |
| **windows**           |                           | Sí      |
| **publisherPolicy**   |                           | Sí      |
|                       | **Aplicar**                 | Sí      |
| **motor en tiempo de ejecución**           |                           | No       |
| **assemblyBinding**   |                           | Sí      |
| **Sondeo**           |                           | No       |
|                       | **privatePath**           | Sí      |
| **Dependencia**        |                           | No       |
| **dependentAssembly** |                           | Sí      |
| **Assemblyidentity**  |                           | Sí      |
|                       | **type**                  | Sí      |
|                       | **name**                  | Sí      |
|                       | **language**              | No       |
|                       | **processorArchitecture** | Sí      |
|                       | **version**               | Sí      |
|                       | **Publickeytoken**        | No       |
| **bindingRedirect**   |                           | Sí      |
|                       | **oldVersion**            | Sí      |
|                       | **newVersion**            | Sí      |



 

## <a name="file-location"></a>Ubicación del archivo

Los archivos de configuración de la aplicación deben instalarse en la misma ubicación que el manifiesto de [aplicación de la aplicación](application-manifests.md).

## <a name="file-name-syntax"></a>Sintaxis de los nombres de archivo

El nombre de un archivo de configuración de la aplicación es el nombre del ejecutable de la aplicación seguido de .config.

Por ejemplo, un archivo de configuración de aplicación que hace referencia a Example.exe o Example.dll usaría la sintaxis de nombre de archivo que se muestra en el ejemplo siguiente. Puede omitir el campo para <identificador de *recurso*> si instala el archivo de configuración como un archivo independiente o si el identificador de recurso es 1.

**example.exe.<*id. de recurso*>.config**

**example.dll.<*id. de recurso*>.config**

## <a name="elements"></a>Elementos

Los nombres de elementos y atributos distinguen mayúsculas de minúsculas. Los valores de elementos y atributos no tienen en cuenta mayúsculas de minúsculas, excepto el valor del atributo de tipo.

<span id="configuration"></span><span id="CONFIGURATION"></span>

### <a name="configuration"></a>configuración

Elemento contenedor para los elementos **windows** y **runtime** de un archivo de configuración de la aplicación. Necesario.

<span id="windows"></span><span id="WINDOWS"></span>

### <a name="windows"></a>Windows

Incluye las partes del archivo de configuración de la aplicación que se aplican al redireccionamiento de ensamblados Win32.

> [!Note]  
> El autor de una aplicación no debe incluir un archivo de configuración con un subelemento **de Windows** como parte de su aplicación. Esto se puede permitir si el único propósito del archivo de configuración es habilitar la funcionalidad **privatePath** de un **elemento de sondeo.** El **elemento de sondeo** no está disponible en sistemas anteriores a Windows Server 2008 R2 y Windows 7.

<span id="publisherPolicy"></span><span id="publisherpolicy"></span><span id="PUBLISHERPOLICY"></span>

### <a name="publisherpolicy"></a>publisherPolicy

Especifica si se debe aplicar la directiva de publicador.

Este elemento tiene los atributos que se muestran en la tabla siguiente.



| Atributo | Descripción                                                                                                                     |
|-----------|---------------------------------------------------------------------------------------------------------------------------------|
| **Aplicar** | Un valor de "sí" aplica la directiva de publicador. Esta es la configuración predeterminada. El valor "no" no aplica la directiva de publicador. |

<span id="runtime"></span><span id="RUNTIME"></span>

### <a name="runtime"></a>motor en tiempo de ejecución

Incluye las partes del archivo de configuración de la aplicación que se aplican al redireccionamiento de ensamblados .NET.

<span id="assemblyBinding"></span><span id="assemblybinding"></span><span id="ASSEMBLYBINDING"></span>

### <a name="assemblybinding"></a>assemblyBinding

Incluye la información de redireccionamiento de la aplicación y el ensamblado afectado por este archivo de configuración de la aplicación. El primer subelemento de **assemblyBinding** debe ser **assemblyIdentity** que identifique la aplicación.

A partir Windows Server 2008 R2 y Windows 7, un elemento **assemblyBinding** puede incluir un **subelemento de** sondeo.

<span id="probing"></span><span id="PROBING"></span>

### <a name="probing"></a>buscar

Subelemento opcional de un **elemento assemblyBinding** que extiende la búsqueda de ensamblados en directorios adicionales. No es necesario que los directorios adicionales sean subdirectorios del directorio del ensamblado.

> [!Note]  
> Este elemento no está disponible en sistemas anteriores a Windows Server 2008 R2 y Windows 7 y solo se puede usar dentro de un **elemento de Windows.**

Este elemento tiene los atributos que se muestran en la tabla siguiente.

| Atributo       | Descripción                                                                                                                                                                                                                                   |
|-----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **privatePath** | Especifica las rutas [de acceso](/windows/desktop/FileIO/naming-a-file) relativas de los subdirectorios del directorio base de la aplicación que pueden contener ensamblados. Se puede especificar un máximo de nueve rutas de acceso de subdirectorio. Delimitar cada ruta de acceso del subdirectorio con un punto y coma. |

Puede usar el especificador especial de dos puntos en una ruta de acceso para indicar el directorio primario del directorio actual. No se pueden especificar más de dos niveles por encima del directorio actual mediante puntos dobles. No use triples puntos. Por ejemplo, una aplicación que usa el siguiente **elemento de sondeo** comprueba directorios adicionales para un ensamblado.

``` XML
<probing privatePath="bin;..\bin2\subbin;bin3"/>
```

<span id="dependency"></span><span id="DEPENDENCY"></span>

### <a name="dependency"></a>dependency
Elemento contenedor para al menos un **elemento dependentAssembly.** Cada **dependentAssembly** puede estar dentro de exactamente una **dependencia**. Este elemento no tiene atributos. Opcional.

<span id="dependentAssembly"></span><span id="dependentassembly"></span><span id="DEPENDENTASSEMBLY"></span>

### <a name="dependentassembly"></a>dependentAssembly

El primer subelemento debe ser un **elemento assemblyIdentity** que identifique el ensamblado en paralelo redirigido por el archivo de configuración de la aplicación. **DependentAssembly** no tiene atributos.

<span id="assemblyIdentity"></span><span id="assemblyidentity"></span><span id="ASSEMBLYIDENTITY"></span>

### <a name="assemblyidentity"></a>assemblyIdentity

Como primer subelemento de un **elemento assemblyBinding,** **assemblyIdentity** describe e identifica de forma única una aplicación. El archivo de configuración de la aplicación redirige el enlace de esta aplicación a ensamblados en paralelo. Por ejemplo, el siguiente **assemblyIdentity** indica que el archivo de configuración de la aplicación afecta al enlace de la aplicación mysampleApp a los ensamblados en paralelo. Los ensamblados que se redirigen se identificarían en **dependentAssembly**.

``` XML
<assemblyIdentity processorArchitecture="X86" name="Microsoft.Windows.mysampleApp" type="win32" version="1.0.0.0"/>
```

Como primer subelemento de un **elemento dependentAssembly,** **assemblyIdentity** describe un ensamblado en paralelo del que depende la aplicación. El archivo de configuración de la aplicación vuelve a configurar la identidad de este ensamblado necesario. Por ejemplo, el **siguiente ensambladoIdentity** y **bindingRedirect** vuelve a configurar una dependencia de Microsoft. Windows. SampleAssembly de la versión 2.0.0.0 a la versión 2.1.0.0.

``` XML
<dependency>
      <dependentAssembly>
         <assemblyIdentity type="win32"
          name="Microsoft.Windows.SampleAssembly"
          processorArchitecture="x86"
          publicKeyToken="0000000000000000"/>
         <bindingRedirect oldVersion="2.0.0.0" newVersion="2.1.0.0"/>
      </dependentAssembly>
</dependency>
```

Tenga en cuenta que todos **los assemblyIdentity** incluidos en **dependentAssembly** deben coincidir exactamente con **assemblyIdentity** en el propio manifiesto [de ensamblado del ensamblado.](assembly-manifests.md)

El **elemento assemblyIdentity** tiene los atributos siguientes. No tiene subelementos.

| Atributo                 | Descripción                                                                                                                                                                                                                                                                                                          |
|---------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **type**                  | El valor debe ser win32 (en minúsculas). Necesario.                                                                                                                                                                                                                                                                      |
| **name**                  | El atributo name identifica la aplicación afectada por el archivo de configuración de la aplicación o el ensamblado que se redirige. Use el formato siguiente para el nombre: Organization.Division.Name. Necesario. Por ejemplo: Microsoft. Windows. MysampleApp o Microsoft. Windows. MysampleAsm.<br/>            |
| **language**              | Identifica el idioma. Opcional. Para un **assemblyIdentity que** hace referencia a un ensamblado, si el ensamblado es específico del lenguaje, especifique el código de lenguaje DHTML. Si el ensamblado es para uso internacional (idioma neutro) establezca el valor en " \* ".<br/>                                                            |
| **processorArchitecture** | Especifica el procesador que ejecuta la aplicación.                                                                                                                                                                                                                                                                     |
| **version**               | Especifica la versión de la aplicación o el ensamblado. Use la sintaxis de la versión de cuatro partes: mmmm.nnnn.oooo.pppp. Necesario.                                                                                                                                                                                                   |
| **Publickeytoken**        | Para un **assemblyIdentity** que hace referencia a un ensamblado, una cadena hexadecimal de 16 caracteres que representa los últimos 8 bytes del hash SHA-1 de la clave pública con la que se firma el ensamblado. La clave pública que se usa para firmar el catálogo debe ser de 2048 bits o superior. Necesario para todos los ensamblados en paralelo compartidos. |

<span id="bindingRedirect"></span><span id="bindingredirect"></span><span id="BINDINGREDIRECT"></span>

### <a name="bindingredirect"></a>bindingRedirect

El **elemento bindingRedirect** contiene información de redirección para el enlace del ensamblado. Cada **bindingRedirect** debe incluirse exactamente en **un elemento dependentAssembly.** La sintaxis de la versión de cuatro partes de la nueva versión y la versión anterior debe especificar las mismas versiones principales y secundarias.

Este elemento tiene los atributos que se muestran en la tabla siguiente.

| Atributo      | Descripción                                                                                                                                                                                                                           |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **oldVersion** | Especifica la versión del ensamblado que se va a invalidar y redirigir. Use la sintaxis de versión de cuatro partes nnnnn.nnnnn.nnnnn.nnnnn. Especifique un intervalo de versiones mediante un guion sin espacios. Por ejemplo, 2.14.3.0 o 2.14.3.0 2.16.0.0. Necesario. |
| **newVersion** | Especifica la versión del ensamblado de reemplazo. Use la sintaxis de versión de cuatro partes nnnnn.nnnnn.nnnnn.nnnnn.                                                                                                                                     |

## <a name="remarks"></a>Observaciones

Los archivos de configuración de la aplicación no especifican archivos.

## <a name="example"></a>Ejemplo

``` XML
<bindingRedirect oldVersion="1.0.0.0" newVersion="1.0.10.0"/>
<bindingRedirect oldVersion="1.0.50.2011-1.0.60.65535" newVersion="1.0.70.0"/>
```
