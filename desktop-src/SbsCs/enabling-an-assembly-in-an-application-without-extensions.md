---
description: Si la aplicación no hospeda un archivo DLL, una extensión, un complemento o un panel de control, puede usar el método descrito en esta sección para habilitar un ensamblado para la aplicación.
ms.assetid: d043ec1b-ac31-45fb-9232-eec42aef4ac3
title: Habilitar un ensamblado en una aplicación sin extensiones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a6666d7b50775438f0d4a3edd13658e5c18127a21c37ec95e46a873682e6f8d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119142258"
---
# <a name="enabling-an-assembly-in-an-application-without-extensions"></a>Habilitar un ensamblado en una aplicación sin extensiones

Si la aplicación no hospeda un archivo DLL, una extensión, un complemento o un panel de control, puede usar el método descrito en esta sección para habilitar un ensamblado para la aplicación. Para obtener más información sobre cómo agregar un ensamblado a aplicaciones con extensiones, vea [Enabling an Assembly in an Application Hosting a DLL, Extension, or Panel de control](enabling-an-assembly-in-an-application-hosting-a-dll-extension-or-control-panel.md).

**Para habilitar un ensamblado en una aplicación sin componentes hospedados**

1.  Cree un manifiesto que describa la dependencia de la aplicación o extensión en el ensamblado.

    Por ejemplo, el manifiesto de "YourApplication" se puede crear copiando el siguiente manifiesto de ejemplo y sustituyendo los valores correctos por **assemblyIdentity**, **processorArchitecture** y **description**. Establezca el valor de **processorArchitecture** en x86 si se está creando en una plataforma de 32 bits y en ia64 si se está creando en una plataforma de 64 bits. El **elemento description** contiene una descripción de opción de la aplicación. Para obtener más información sobre el formato de manifiesto, vea [manifiestos de aplicación.](application-manifests.md)

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

2.  Agregue el manifiesto a la aplicación como un recurso en el archivo de encabezado ejecutable binario de la aplicación. No se recomienda agregar el manifiesto a la aplicación como un archivo de manifiesto externo.

    Para agregar el manifiesto como un recurso, cree un recurso en la aplicación de tipo RT \_ MANIFEST id 1. Por ejemplo, si el nombre de la aplicación es YourApp, el archivo de encabezado de la aplicación debe contener lo siguiente:

    ``` syntax
    #define MANIFEST_RESOURCE_ID 1
    MANIFEST_RESOURCE_ID RT_MANIFEST "YourApp.manifest"
    ```

    Si en su lugar agrega el manifiesto como un archivo de manifiesto externo, asegúrese de que la instalación copia el archivo de manifiesto en la carpeta que contiene el archivo ejecutable de la aplicación.

3.  Pruebe para asegurarse de que los ensamblados usados por la aplicación funcionan correctamente en la aplicación.

 

 



