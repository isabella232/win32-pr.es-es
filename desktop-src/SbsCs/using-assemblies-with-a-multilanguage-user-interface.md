---
description: Si desea que los usuarios de la aplicación, o el archivo DLL principal, puedan cambiar el idioma de la interfaz de usuario, considere la posibilidad de colocar los recursos de idioma en archivos dll de recursos satélite independientes.
ms.assetid: fcadd7e8-cab8-43cb-9c67-af8ebe0e3a5b
title: Uso de ensamblados con una interfaz de usuario multilingüe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77f501f40715dc2335f02c044aa48ada9741411d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809361"
---
# <a name="using-assemblies-with-a-multilanguage-user-interface"></a>Uso de ensamblados con una interfaz de usuario multilingüe

Si desea que los usuarios de la aplicación, o el archivo DLL principal, puedan cambiar el idioma de la interfaz de usuario, considere la posibilidad de colocar los recursos de idioma en archivos dll de recursos satélite independientes. Para obtener más información sobre el uso de archivos dll de recursos satélite, consulte [interfaz de usuario multilingüe (MUI)](/windows/desktop/Intl/multilingual-user-interface).

Cada archivo DLL satélite contiene los recursos de un idioma diferente. El archivo DLL principal se puede proporcionar como un ensamblado y cada uno de los archivos dll satélite se puede proporcionar como ensamblados satélite independientes. En este caso, cada ensamblado satélite debe tener su propio manifiesto de ensamblado autodescriptivo. El manifiesto del ensamblado satélite no debe describir ninguna dependencia de otros ensamblados. En su lugar, se debe describir cualquier dependencia de ensamblados satélite en otros ensamblados en el manifiesto del ensamblado principal.

La versión de la [interfaz de usuario multilingüe (MUI)](/windows/desktop/Intl/multilingual-user-interface) de Windows permite a los usuarios especificar el idioma de la interfaz de usuario de acuerdo con sus preferencias, siempre que se haya agregado el idioma requerido al sistema. Un ensamblado principal puede admitir varios idiomas mediante el uso de varios ensamblados MUI. En este caso, cada ensamblado MUI debe tener su propio manifiesto y todas las dependencias de otros ensamblados deben describirse solo en el manifiesto del ensamblado principal.

Por ejemplo, Proseware. sample. pop puede ser un ensamblado en paralelo básico que es dependiente del ensamblado Proseware. Research. SampleAssembly. Si Proseware. sample. pop usa MUI para admitir varios idiomas, se pueden proporcionar ensamblados MUI independientes para cada idioma. Cada ensamblado MUI debe tener su propio manifiesto que describe este archivo DLL de recursos satélite determinado. Los manifiestos de ensamblado de MUI no deben incluir ninguna referencia a las dependencias de otros ensamblados. El manifiesto que describe el ensamblado principal, Proseware. sample. pop, debe describir la dependencia de Proseware. sample. pop en el ensamblado Proseware. Research. SampleAssembly.

Los atributos del elemento **assemblyIdentity** de un ensamblado satélite son similares a los del manifiesto del ensamblado base. El atributo **Name** debe ser el mismo que el ensamblado base con la adición de "Resources". Por ejemplo, si el nombre es "Proseware. Tools. corrector. Runtime-Libraries" en el ensamblado base, el nombre en el ensamblado de recursos sería "Proseware. Tools. de corrección. Runtime-Libraries. Resources". El atributo **Language** debe identificar el idioma del ensamblado del recurso. El atributo de **archivo** debe incluir la lista de archivos dll de recursos.

El siguiente es un ejemplo del manifiesto del ensamblado de los recursos de Proseware. Tools. revisor. Runtime-Libraries.

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

El ensamblado base describe una dependencia opcional en el ensamblado de recursos. En este ejemplo, si un usuario ejecuta Windows con la configuración regional designada como alemán, una aplicación que use el ensamblado Proseware. Tools. de ortografía mostraría el texto en alemán.

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

 

 
