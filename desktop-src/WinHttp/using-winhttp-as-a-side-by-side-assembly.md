---
description: En Windows Server 2003, WinHTTP se implementa como un ensamblado en paralelo y debe vincularse como tal. Tenga en cuenta que esto no se aplica a Windows Vista y versiones posteriores.
ms.assetid: 524d926d-4d8a-4576-96fd-c533517ba28e
title: Uso de WinHTTP como ensamblado en paralelo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f682586ba315932d8dc7812f7e74bd15e20e4ad6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127568176"
---
# <a name="using-winhttp-as-a-side-by-side-assembly"></a>Uso de WinHTTP como ensamblado en paralelo

En Windows Server 2003, WinHTTP se implementa como un ensamblado en paralelo y debe vincularse como tal. Tenga en cuenta que esto no se aplica a Windows Vista y versiones posteriores.

## <a name="side-by-side-assemblies"></a>Ensamblados en paralelo

A partir de Microsoft Windows XP, se proporcionó un mecanismo de ensamblados en paralelo para controlar la vinculación en tiempo de ejecución con el fin de evitar conflictos de control de versiones de dynamic-link-library (DLL). Para obtener información sobre los ensamblados en paralelo, vea Acerca de las aplicaciones aisladas y los ensamblados [en paralelo.](/windows/desktop/SbsCs/about-isolated-applications-and-side-by-side-assemblies)

Para usar este mecanismo para vincular a la versión 5.1 de WinHTTP en Windows Server 2003, una aplicación debe incorporar un manifiesto que especifique WinHTTP como ensamblado dependiente. Vea [Using Side-by-side Assemblies (Uso](/windows/desktop/SbsCs/using-side-by-side-assemblies) de ensamblados en paralelo) para obtener más información sobre cómo hacerlo.

## <a name="a-sample-winhttp-application-manifest"></a>Un manifiesto de aplicación WinHTTP de ejemplo

En el siguiente manifiesto de ejemplo se muestra un manifiesto de aplicación que se puede usar para vincular a WinHTTP.

Todos los atributos excepto "type" de " &lt; &gt; &lt; assembly assemblyIdentity " deben modificarse según &gt; corresponda para la aplicación en particular. Lo mismo sucede con el contenido del elemento " &lt; description &gt; ".

Además, asegúrese de que el atributo "processorArchitecture" de " dependentAssembly assemblyIdentity " coincide con el atributo &lt; &gt; &lt; &gt; "processorArchitecture" del ensamblado &lt; &gt; &lt; assemblyIdentity &gt; ". A continuación, por ejemplo, ambos se establecen en "x86".

Todos los valores no específicos de la aplicación deben tener los formularios que se muestran a continuación.

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
  <assemblyIdentity
                    version="1.0.0.0"
                    processorArchitecture="x86"
                    name="Microsoft.Windows.Sample"
                    type="win32" />
  <description>Sample WinHttp Application</description>
  <dependency>
    <dependentAssembly>
      <assemblyIdentity 
                    type="win32" 
                    name="Microsoft.Windows.WinHTTP" 
                    version="5.1.0.0"
                    processorArchitecture="x86" 
                    publicKeyToken="6595b64144ccf1df"
                    language="*" />
    </dependentAssembly>
  </dependency>
</assembly>
```

 

 
