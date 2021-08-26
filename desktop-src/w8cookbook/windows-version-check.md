---
title: Comprobación de la versión de Windows
description: La versión del sistema operativo se ha incrementado con la Windows 10 del sistema operativo.
ms.assetid: 55BB7B44-1AFD-456D-9380-38B4D26E5EF6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 710f59313f05dac95e5953c6013108987dc9bf8ad84d7eb7d8bca67a5391996b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120007885"
---
# <a name="windows-version-check"></a>Comprobación de la versión de Windows

La versión del sistema operativo se ha incrementado con la Windows 10 del sistema operativo. Esto significa que el número de versión interno de Windows 10 también se ha cambiado a 10.0. Como ya sucedió en su día, hacemos todo lo posible para mantener la compatibilidad de los dispositivos y las aplicaciones tras un cambio de versión del sistema operativo. En la mayoría de las categorías de aplicaciones (sin dependencias de kernel), el cambio no afectará negativamente a la funcionalidad de la aplicación y las aplicaciones existentes seguirán funcionando correctamente en Windows 10.

## <a name="manifestations"></a>Manifestaciones

La manifestación de este cambio es específica de cada aplicación. Esto significa que cualquier aplicación que compruebe específicamente la versión del sistema operativo obtendrá un número de versión superior, lo que puede ocasionar una o varias de las siguientes situaciones:

-   Es posible que los instaladores de aplicaciones no puedan instalar la aplicación y que las aplicaciones no puedan iniciarse.
-   Las aplicaciones podrían volverse inestables o bloquearse.
-   Las aplicaciones podrían generar mensajes de error, pero seguir funcionando correctamente.

Algunas aplicaciones realizan una comprobación de la versión y simplemente muestran una advertencia a los usuarios. Sin embargo, hay aplicaciones que están enlazadas muy estrechamente a una comprobación de la versión (por ejemplo, en los controladores o en el modo kernel para evitar la detección). En estos casos, si se encuentra una versión incorrecta, se producirá un error en la aplicación. En lugar de una comprobación de la versión, recomendamos uno de los siguientes métodos:

-   Si la aplicación depende de la funcionalidad de una API específica, asegúrate de que apuntas a la versión correcta de dicha API.
-   El número de versión de NTDDI (interfaz del controlador de dispositivo NT) se incrementará solo si cambia la funcionalidad de destino en la API. Asegúrese de detectar el cambio a través de APISet u otra API expuesta creada por el equipo de características y no use la versión como proxy para alguna característica o corrección. Si hay cambios importantes y no se expone una comprobación adecuada, se trata de un error.
-   Asegúrese de que la aplicación NO comprueba la versión de maneras impares, como a través del Registro, las versiones de archivo, los desplazamientos, el modo kernel, los controladores u otros medios. Si la aplicación necesita comprobar la versión, use las API de GetVersion, que deben devolver el número principal, menor y de compilación.
-   Si usa la API GetVersion u otras funciones del asistente de versiones como [VerifyVersionInfo,](/windows/desktop/api/winbase/nf-winbase-verifyversioninfoa)recuerde que el comportamiento de esta API ha cambiado a partir de Windows 8.1. Consulte la documentación [de la API para](../SysInfo/version-helper-apis.md) obtener más detalles.
-   Si posee aplicaciones como antimalware o firewall, debe trabajar a través de los canales de comentarios habituales y a través del programa Windows Insider.

## <a name="declaring-windows-10-compatibility-with-an-app-manifest"></a>Declarar Windows 10 compatibilidad con un manifiesto de aplicación

Si la aplicación es compatible con Windows 10, puede declarar este hecho en el manifiesto de aplicación [(ejecutable)](/windows/compatibility/application-executable-manifest) para el ejecutable de la aplicación. Esto indica al sistema que la aplicación entiende el número de versión del sistema de Windows 10 de 10.0 (por lo que la API GetVersion no devuelve una versión anterior) y también permite que el sistema desactive otros comportamientos de compatibilidad aplicados a las aplicaciones que no declaran compatibilidad con Windows 10.

Para declarar la compatibilidad de Windows 10 en un manifiesto de [ **&lt; &gt;**](../SbsCs/application-manifests.md#compatibility) aplicación, deberá agregar una sección de compatibilidad del manifiesto si aún no existe y, a continuación, agregar elementos **&lt; supportedOS &gt;** para Windows 10 y todas las demás versiones de Windows que quiera declarar que la aplicación admite.

En el ejemplo siguiente se muestra un archivo de manifiesto de aplicación para una aplicación que admite todas las versiones de Windows de Windows Vista a Windows 10:

```XML
<!-- example.exe.manifest -->
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly manifestVersion="1.0" xmlns="urn:schemas-microsoft-com:asm.v1" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3">
    <assemblyIdentity
        type="win32"
        name="Contoso.ExampleApplication.ExampleBinary"
        version="1.2.3.4"
        processorArchitecture="x86"
    />
    <description>Contoso Example Application</description>
    <compatibility xmlns="urn:schemas-microsoft-com:compatibility.v1">
        <application>
            <!-- Windows 10 -->
            <supportedOS Id="{8e0f7a12-bfb3-4fe8-b9a5-48fd50a15a9a}"/> <!-- * ADD THIS LINE * -->
            <!-- Windows 8.1 -->
            <supportedOS Id="{1f676c76-80e1-4239-95bb-83d0f6d0da78}"/>
            <!-- Windows 8 -->
            <supportedOS Id="{4a2f28e3-53b9-4441-ba9c-d69d4a4a6e38}"/>
            <!-- Windows 7 -->
            <supportedOS Id="{35138b9a-5d96-4fbd-8e2d-a2440225f93a}"/>
            <!-- Windows Vista -->
            <supportedOS Id="{e2011457-1546-43c5-a5fe-008deee3d3f0}"/> 
        </application>
    </compatibility>
</assembly>
```

La línea anterior marcada `* ADD THIS LINE *` muestra cómo dirigirse con precisión a la aplicación para Windows 10.

Declarar la compatibilidad con Windows 10 en el manifiesto de aplicación no tendrá ningún efecto al ejecutar la aplicación en sistemas operativos anteriores.

## <a name="resources"></a>Recursos

-   [Descarga de Toolkit compatibilidad de aplicaciones: descargue el Windows ADK para Windows 10](https://download.microsoft.com/download/9/A/E/9AE69DD5-BA93-44E0-864E-180F5E700AB4/adk/adksetup.exe)
-   [Correcciones de compatibilidad conocidas, modos de compatibilidad y mensajes de AppHelp](/previous-versions/windows/it-pro/windows-7/cc765984(v=ws.10))
-   [API de asistentes de versiones](../sysinfo/version-helper-apis.md)