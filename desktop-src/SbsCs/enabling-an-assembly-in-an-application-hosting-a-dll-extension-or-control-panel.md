---
description: Si la aplicación hospeda un archivo DLL, una extensión, un complemento o un panel de control de terceros, es posible que desee habilitar un ensamblado en la aplicación&\# 8212; sin habilitar también este ensamblado para los componentes hospedados.
ms.assetid: 832957ca-82fc-4600-b469-512621dde921
title: Habilitar un ensamblado en una aplicación que hospeda un archivo DLL, una extensión o un panel de control
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b04dd19b18c2cdce4783be47333b9afe53dd1ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105648429"
---
# <a name="enabling-an-assembly-in-an-application-hosting-a-dll-extension-or-control-panel"></a>Habilitar un ensamblado en una aplicación que hospeda un archivo DLL, una extensión o un panel de control

Si la aplicación hospeda un archivo DLL, una extensión, un complemento o un panel de control de terceros, es posible que desee habilitar un ensamblado en la aplicación, sin habilitar también este ensamblado para los componentes hospedados. Este puede ser el caso cuando un componente hospedado requiere cambios en el código para usar el ensamblado. Como desarrollador de la aplicación, es posible que no pueda realizar cambios en estos componentes de terceros. En este caso, debe seguir el procedimiento descrito en esta sección para que la aplicación pueda utilizar el ensamblado sin que afecte a los componentes hospedados.

-   Para habilitar un ensamblado en una aplicación sin afectar a los archivos dll, extensiones, complementos o paneles de control hospedados, se debe incluir en la aplicación como un recurso un manifiesto que describa la dependencia de la aplicación en el ensamblado. Los componentes hospedados que no se habilitan con el ensamblado no deben incluir manifiestos que describan esta dependencia.
-   Para habilitar un ensamblado en una aplicación y sus archivos dll, extensiones, complementos o paneles de control hospedados, incluya manifiestos como recursos tanto en la aplicación como en sus componentes hospedados. Los manifiestos incluidos en la aplicación y en los componentes hospedados deben describir una dependencia en el ensamblado. Normalmente, el desarrollador de la aplicación agrega un manifiesto a la aplicación y el desarrollador del componente hospedado agrega un manifiesto al archivo DLL, la extensión, el complemento o el panel de control.

El método siguiente se puede usar para agregar un manifiesto a una aplicación o un componente hospedado que sea un archivo DLL, una extensión, un complemento o un panel de control.

**Para habilitar un ensamblado en una aplicación o componente hospedado.**

1.  Cree un manifiesto que describa la dependencia de la aplicación o extensión en el ensamblado.

    Por ejemplo, el manifiesto de "YourApplication" se puede crear copiando el siguiente manifiesto de ejemplo y sustituyendo los valores correctos para **assemblyIdentity**, **processorArchitecture** y **Description**. Establezca el valor de **processorArchitecture** en x86 si se compila en una plataforma de 32 bits y en IA64 si se compila en una plataforma de 64 bits. El elemento **Description** contiene una descripción de la opción de la aplicación. Para obtener más información sobre el formato de manifiesto, consulte [manifiestos de aplicación](application-manifests.md).

    ``` syntax
    <?xml version="1.0" encoding="UTF-8" standalone="yes"?>
    <assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
    <assemblyIdentity
        version="1.0.0.0"
        processorArchitecture="x86"
        name="YourCompanyName.YourDivision.YourApp"
        type="win32"
    />
    <description>Your app description here</description>
    <dependency>
        <dependentAssembly>
            <assemblyIdentity
                type="win32"
                name="Proseware.Research.SampleAssembly"
                version="6.0.0.0"
                processorArchitecture="X86"
                publicKeyToken="0000000000000000"
                language="*"
            />
        </dependentAssembly>
    </dependency>
    </assembly>
    ```

2.  Cree un recurso en la aplicación o la extensión de tipo RT \_ manifest ID 2.

    Por ejemplo, si el nombre de la aplicación es outName, la aplicación debe contener lo siguiente:

    ``` syntax
    #define MANIFEST_RESOURCE_ID 2
    MANIFEST_RESOURCE_ID RT_MANIFEST "YourApp.manifest"
    ```

3.  Compile la aplicación con la marca-DISOLATION \_ compatible \_ habilitada o inserte esta instrucción antes de la \# instrucción include "Windows. h". En el caso de una aplicación con varios módulos, \_ se requiere la marca-DISOLATION compatible \_ habilitada en todos los módulos.

    ``` syntax
    #define ISOLATION_AWARE_ENABLED 1
    ```

4.  Pruebe para asegurarse de que los ensamblados utilizados por la aplicación funcionan correctamente en la aplicación y en el componente hospedado.

Para obtener más información sobre cómo agregar un ensamblado a aplicaciones sin extensiones, vea [habilitar un ensamblado en una aplicación sin extensiones](enabling-an-assembly-in-an-application-without-extensions.md).

 

 



