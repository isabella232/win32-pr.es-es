---
description: Si desea que los usuarios de la aplicación, o dll principal, sean capaces de cambiar el idioma de la interfaz de usuario, considere la posibilidad de colocar recursos de idioma en archivos DLL de recursos satélite independientes.
ms.assetid: fcadd7e8-cab8-43cb-9c67-af8ebe0e3a5b
title: Usar ensamblados con un lenguaje multilenguaje Interfaz de usuario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4cd857cca0188b10f02ba44b5631895a9345ce7926cae78376edd554035ccfc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119141778"
---
# <a name="using-assemblies-with-a-multilanguage-user-interface"></a>Usar ensamblados con un lenguaje multilenguaje Interfaz de usuario

Si desea que los usuarios de la aplicación, o dll principal, sean capaces de cambiar el idioma de la interfaz de usuario, considere la posibilidad de colocar recursos de idioma en archivos DLL de recursos satélite independientes. Para obtener más información sobre el uso de archivos DLL de recursos satélite, vea [Multilanguage Interfaz de usuario (MUI).](/windows/desktop/Intl/multilingual-user-interface)

Cada archivo DLL satélite contiene los recursos de un lenguaje diferente. El archivo DLL principal se puede proporcionar como un ensamblado y cada uno de los archivos DLL satélite se puede proporcionar como ensamblados satélite independientes. En este caso, cada ensamblado satélite debe tener su propio manifiesto de ensamblado autodescripto. El manifiesto del ensamblado satélite no debe describir ninguna dependencia de otros ensamblados. Cualquier dependencia de ensamblados satélite en otros ensamblados debe describirse en su lugar en el manifiesto del ensamblado principal.

La [versión multilenguaje Interfaz de usuario (MUI)](/windows/desktop/Intl/multilingual-user-interface) de Windows permite a los usuarios especificar el idioma de la interfaz de usuario según sus preferencias, siempre que el idioma necesario se haya agregado al sistema. Un ensamblado principal puede admitir varios lenguajes mediante el uso de varios ensamblados de MUI. En este caso, cada ensamblado de MUI debe tener su propio manifiesto y las dependencias de otros ensamblados solo se deben describir en el manifiesto del ensamblado principal.

Por ejemplo, Proseware.Sample.Pop puede ser un ensamblado en paralelo básico que depende del ensamblado Proseware.Research.SampleAssembly. Si Proseware.Sample.Pop usa LAN para admitir varios idiomas, se pueden proporcionar ensamblados DE EXTENSIÓN independientes para cada idioma. Cada ensamblado de MUI debe tener su propio manifiesto que describa este archivo DLL de recursos satélite concreto. Los manifiestos de ensamblado de MUI no deben incluir ninguna referencia a las dependencias de otros ensamblados. El manifiesto que describe el ensamblado principal, Proseware.Sample.Pop, debe describir la dependencia de Proseware.Sample.Pop en el ensamblado Proseware.Research.SampleAssembly.

Los atributos del elemento **assemblyIdentity** de un ensamblado satélite son similares a los del manifiesto del ensamblado base. El **atributo** name debe ser el mismo que el ensamblado base con la adición de "Resources". Por ejemplo, si el nombre es "Proseware.Tools.SpellCheck.Runtime-Libraries" en el ensamblado base, el nombre del ensamblado de recursos sería "Proseware.Tools.SpellCheck.Runtime-Libraries.Resources". El **atributo language** debe identificar el idioma del ensamblado de recursos. El **atributo** file debe incluir la lista de archivos dll de recursos.

A continuación se muestra un ejemplo del manifiesto para el ensamblado de recursos Proseware.Tools.SpellCheck.Runtime-Libraries.

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
    <assemblyIdentity
        type="win32"
        name="Proseware.Tools.SpellCheck.Runtime-Libraries.Resources"
        version="6.0.0.0"
        processorArchitecture="X86"
        language="DE"
        publicKeyToken="0000000000000000"
    />
    <file name="sample.dll"/>
</assembly>
```

El ensamblado base describe una dependencia opcional en el ensamblado de recursos. En este ejemplo, si un usuario ejecuta Windows con la configuración regional designada como alemán, una aplicación que usa el ensamblado Proseware.Tools.SpellCheck mostraría texto en alemán.

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
    <assemblyIdentity type="win32" 
    name="Proseware.Tools.SpellCheck.Runtime-Libraries"
    version="6.0.0.0" processorArchitecture="x86"
    publicKeyToken="0000000000000000"/>
    <dependency optional="yes">
        <dependentAssembly>
            <assemblyIdentity type="win32" 
                              name="Proseware.Tools.SpellCheck.Runtime-Libraries.Resources" 
                              version="6.0.0.0" 
                              processorArchitecture="x86" 
                              publicKeyToken="0000000000000000" 
                              language="*"
            />
        </dependentAssembly>
    </dependency>
```

 

 
