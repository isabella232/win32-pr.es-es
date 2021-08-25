---
description: Si la aplicación hospeda un archivo DLL de terceros, una extensión, un complemento o un panel de control, es posible que desee habilitar un ensamblado en la aplicación&8212; sin habilitar también este ensamblado para los componentes \# hospedados.
ms.assetid: 832957ca-82fc-4600-b469-512621dde921
title: Habilitar un ensamblado en una aplicación que hospeda un archivo DLL, una extensión o una Panel de control
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23ac528c10d7ca0de903c6b132e0349c16061d63f121c390483458b4ef422d66
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119885545"
---
# <a name="enabling-an-assembly-in-an-application-hosting-a-dll-extension-or-control-panel"></a>Habilitar un ensamblado en una aplicación que hospeda un archivo DLL, una extensión o una Panel de control

Si la aplicación hospeda un archivo DLL de terceros, una extensión, un complemento o un panel de control, puede que desee habilitar un ensamblado en la aplicación, sin habilitar también este ensamblado para los componentes hospedados. Esto puede ser así cuando un componente hospedado requiere cambios de código para usar el ensamblado. Como desarrollador de aplicaciones, es posible que no pueda realizar cambios en estos componentes de terceros. En este caso, debe seguir el procedimiento descrito en esta sección para que la aplicación pueda usar el ensamblado sin afectar a los componentes hospedados.

-   Para habilitar un ensamblado en una aplicación sin que afecte a ningún archivo DLL hospedado, extensiones, complementos o paneles de control, se debe incluir en la aplicación como recurso un manifiesto que describa la dependencia de la aplicación en el ensamblado. Los componentes hospedados que no se habilitan con el ensamblado no deben incluir manifiestos que describan esta dependencia.
-   Para habilitar un ensamblado en una aplicación y sus archivos DLL hospedados, extensiones, complementos o paneles de control, incluya manifiestos como recursos tanto en la aplicación como en sus componentes hospedados. Los manifiestos incluidos en la aplicación y en los componentes hospedados deben describir cada uno una dependencia del ensamblado. Normalmente, el desarrollador de la aplicación agrega un manifiesto a la aplicación y el desarrollador del componente hospedado agrega un manifiesto al archivo DLL, la extensión, el complemento o el panel de control.

El método siguiente se puede usar para agregar un manifiesto a una aplicación o un componente hospedado que sea un archivo DLL, una extensión, un complemento o un panel de control.

**Para habilitar un ensamblado en una aplicación o un componente hospedado.**

1.  Cree un manifiesto que describa la dependencia de la aplicación o la extensión en el ensamblado.

    Por ejemplo, el manifiesto de "YourApplication" se puede crear copiando el siguiente manifiesto de ejemplo y sustituyendo los valores correctos por **assemblyIdentity**, **processorArchitecture** y **description**. Establezca el valor de **processorArchitecture** en x86 si se está creando en una plataforma de 32 bits y en ia64 si se está creando en una plataforma de 64 bits. El **elemento description** contiene una descripción de opción de la aplicación. Para obtener más información sobre el formato de manifiesto, vea [Manifiestos de aplicación.](application-manifests.md)

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

2.  Cree un recurso en la aplicación o extensión de tipo RT \_ MANIFEST id. 2.

    Por ejemplo, si el nombre de la aplicación es YourApp, la aplicación debe contener lo siguiente:

    ``` syntax
    #define MANIFEST_RESOURCE_ID 2
    MANIFEST_RESOURCE_ID RT_MANIFEST "YourApp.manifest"
    ```

3.  Compile la aplicación con la marca -DISOLATION AWARE ENABLED o inserte esta instrucción antes de incluir \_ \_ la instrucción \# "Windows.h". En el caso de una aplicación con varios módulos, se requiere la marca -DISOLATION \_ AWARE ENABLED en todos los \_ módulos.

    ``` syntax
    #define ISOLATION_AWARE_ENABLED 1
    ```

4.  Pruebe para asegurarse de que los ensamblados utilizados por la aplicación funcionan correctamente en la aplicación y el componente hospedado.

Para obtener más información sobre cómo agregar un ensamblado a aplicaciones sin extensiones, vea [Habilitar un ensamblado en una aplicación sin extensiones.](enabling-an-assembly-in-an-application-without-extensions.md)

 

 



