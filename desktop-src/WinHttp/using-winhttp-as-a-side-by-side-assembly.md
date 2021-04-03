---
description: En Windows Server 2003, WinHTTP se implementa como un ensamblado en paralelo y debe estar vinculado a como tal. Tenga en cuenta que esto no se aplica a Windows Vista y versiones posteriores.
ms.assetid: 524d926d-4d8a-4576-96fd-c533517ba28e
title: Usar WinHTTP como un ensamblado en paralelo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a74a0e5cf842fdd1e20c6d6d271de482e361c4af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809782"
---
# <a name="using-winhttp-as-a-side-by-side-assembly"></a>Usar WinHTTP como un ensamblado en paralelo

En Windows Server 2003, WinHTTP se implementa como un ensamblado en paralelo y debe estar vinculado a como tal. Tenga en cuenta que esto no se aplica a Windows Vista y versiones posteriores.

## <a name="side-by-side-assemblies"></a>Ensamblados en paralelo

A partir de Microsoft Windows XP, se proporciona un mecanismo de ensamblados en paralelo para controlar la vinculación en tiempo de ejecución para evitar conflictos de versiones de la biblioteca de vínculos dinámicos (DLL). Para obtener información sobre los ensamblados en paralelo, vea [acerca de las aplicaciones aisladas y los ensamblados en paralelo](/windows/desktop/SbsCs/about-isolated-applications-and-side-by-side-assemblies).

Para usar este mecanismo para vincular a la versión 5,1 de WinHTTP en Windows Server 2003, una aplicación debe incorporar un manifiesto que especifique WinHTTP como ensamblado dependiente. Vea [usar ensamblados en paralelo](/windows/desktop/SbsCs/using-side-by-side-assemblies) para obtener más información sobre cómo hacerlo.

## <a name="a-sample-winhttp-application-manifest"></a>Un manifiesto de aplicación WinHTTP de ejemplo

En el manifiesto de ejemplo siguiente se muestra un manifiesto de aplicación que se puede usar para vincular a WinHTTP.

Todos los atributos excepto "tipo" de " <assembly> <assemblyIdentity> " se deben modificar según sea necesario para la aplicación en cuestión. Lo mismo sucede con el contenido del elemento " &lt; Description &gt; ".

Además, asegúrese de que el atributo "processorArchitecture" de " <dependentAssembly> <assemblyIdentity> " coincide con el atributo "processorArchitecture" de " <assembly> <assemblyIdentity> ". A continuación, por ejemplo, ambos se establecen en "x86".

Todos los valores que no son específicos de la aplicación deben tener los formularios que se muestran a continuación.

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

 

 
