---
title: Desarrollo de aplicaciones para versiones anteriores de Windows
description: Explica qué hacer para desarrollar aplicaciones que se ejecutan en versiones anteriores de Windows y aprovechar las ventajas de la API que se admiten con la actualización de la plataforma para Windows Vista y la actualización de la plataforma para Windows Server 2008.
ms.assetid: 9c46f894-e5cd-46a1-81c8-f63b09504735
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 299d4c61b0e2b931c3833934c843bf964fc3fa7c
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "104424159"
---
# <a name="developing-applications-for-previous-versions-of-windows"></a>Desarrollo de aplicaciones para versiones anteriores de Windows

Explica qué hacer para desarrollar aplicaciones que se ejecutan en versiones anteriores de Windows y aprovechar las ventajas de la API que se admiten con la actualización de la plataforma para Windows Vista y la actualización de la plataforma para Windows Server 2008.

## <a name="required-downloads"></a>Descargas necesarias

La descarga e instalación de los paquetes que se describen en las siguientes secciones es necesaria si desea desarrollar aplicaciones que usan la API que se introdujeron con el kit de desarrollo de software (SDK) de Microsoft Windows para Windows 7.

### <a name="microsoft-windows-sdk"></a>Microsoft Windows SDK

La Windows SDK para Windows 7 es necesaria para crear aplicaciones que usan las API compatibles con la actualización de la plataforma para Windows Vista y la actualización de la plataforma para Windows Server 2008.

Para obtener acceso a recursos e información adicionales, como descargas, publicaciones de foros y el blog del equipo de Windows SDK, consulte el [Centro para desarrolladores de Windows SDK](https://msdn.microsoft.com/bb980924.aspx) ( https://msdn.microsoft.com/bb980924.aspx) .

### <a name="net-framework"></a>.NET Framework

Se necesita el Service Pack 1 de .NET Framework 3,5 para crear aplicaciones que usan las API admitidas por la actualización de la plataforma para Windows Vista y la actualización de la plataforma para Windows Server 2008.

Para obtener más recursos e información, vea el [Centro para desarrolladores de .NET Framework](https://msdn.microsoft.com/netframework/default.aspx) ( https://msdn.microsoft.com/netframework/default.aspx) .

### <a name="directx-sdk-required-when-using-direct3d"></a>DirectX SDK necesario al usar Direct3D

Si crea aplicaciones que usan Direct3D, el [SDK de DirectX](/previous-versions/windows/apps/hh452744(v=win.10)) ( https://msdn.microsoft.com/directx/aa937788.aspx) es necesario para crear aplicaciones que usan las API admitidas por la actualización de la plataforma para Windows Vista y la actualización de la plataforma para Windows Server 2008.

### <a name="update-your-development-computer"></a>Actualización del equipo de desarrollo

Asegúrese de que el equipo de desarrollo tenga todas las actualizaciones más recientes de Windows Update.

Si va a desarrollar aplicaciones en una versión anterior de Windows, debe obtener la actualización de la plataforma para Windows Vista o la actualización de la plataforma para Windows Server 2008 desde Windows Update. La instalación de cualquiera de estas actualizaciones le permitirá aprovechar la nueva API proporcionada por el Windows SDK para Windows 7.

Para obtener más información acerca de cómo obtener actualizaciones de Windows Update vea el [artículo de Knowledge Base acerca de la actualización de la plataforma para Windows Vista (KB 971644)](https://support.microsoft.com/kb/971644) ( https://support.microsoft.com/kb/971644) .

## <a name="development-environment"></a>Entorno de desarrollo

### <a name="set-the-build-target-to-windows-7"></a>Establecer el destino de compilación en Windows 7

Todas las aplicaciones que usan bibliotecas en la actualización de la plataforma para Windows Vista deben compilarse en la plataforma de destino de Windows 7.

Establecer WINVER en el valor de la plataforma de destino de Windows 7 le permite desarrollar aplicaciones que usan las API compatibles con la actualización de la plataforma para Windows Vista o la actualización de la plataforma para Windows Server 2008 en una máquina de desarrollo que ejecuta Windows Vista.

Puede establecer la plataforma de destino en Windows 7, ya sea en el código fuente o mediante la opción/D con el compilador de Visual Studio.

En el ejemplo siguiente se muestra cómo establecer WINVER en el código fuente.


```C++
#define WINVER 0x0601
```



En el ejemplo siguiente se muestra cómo establecer WINVER mediante la opción del compilador/D.

``` syntax
/DWINVER=0x0601
```

## <a name="application-deployment"></a>Implementación de aplicaciones

Si compila la aplicación mediante los encabezados y las bibliotecas proporcionadas por el Windows SDK para Windows 7, las API admitidas se ejecutarán en cualquier versión de Windows que tenga instalada la actualización de la plataforma para Windows Vista o la actualización de la plataforma para Windows Server 2008.

> [!Note]  
> El comportamiento, el rendimiento o los requisitos de algunas API que son compatibles con la actualización de la plataforma para Windows Vista o la actualización de la plataforma para Windows Server 2008 pueden variar en diferentes versiones de Windows. Para obtener más información acerca de una API específica que es compatible con las actualizaciones, vea acerca de la [actualización de la plataforma para Windows Vista](platform-update-for-windows-vista-overview.md).

 

### <a name="no-redistributable-components"></a>No hay componentes redistribuibles

No es necesario que la aplicación Instale componentes redistribuibles, como archivos dll u otros archivos en tiempo de ejecución.

### <a name="requires-updated-end-user-computer"></a>Requiere End-User equipo actualizado

Dado que la actualización de la plataforma para Windows Vista y la actualización de plataforma para Windows Server 2008 se hospedan en Windows Update, es muy probable que los usuarios finales con actualizaciones automáticas habilitadas ya tengan estas actualizaciones y los Service Packs necesarios.

Si el equipo del usuario final no tiene instalada la actualización de la plataforma para Windows Vista o la actualización de la plataforma para Windows Server 2008 y la aplicación requiere API compatibles con estas actualizaciones, es posible que la aplicación no se pueda ejecutar en el equipo del usuario final o que se produzcan errores durante la ejecución.

Para evitar los problemas que podrían deberse a que el equipo del usuario no está actualizado, desea comprobar que el equipo del usuario tiene la actualización de la plataforma para Windows Vista o la actualización de la plataforma para Windows Server 2008 durante la instalación de la aplicación. Puede usar la [API del agente de Windows Update](/windows/desktop/Wua_Sdk/portal-client) para comprobar si el equipo del usuario final tiene actualizaciones instaladas. También puede usar la API del agente de Windows Update para descargar e instalar las actualizaciones necesarias durante la instalación de la aplicación si el usuario final no ha instalado ya las actualizaciones.

Para obtener un ejemplo de un instalador que muestra cómo usar la [API del agente de Windows Update](/windows/desktop/Wua_Sdk/portal-client), vea [implementación de Direct3D 11 para desarrolladores de juegos](../direct3darticles/direct3d11-deployment.md) en el SDK de [DirectX](/previous-versions/windows/apps/hh452744(v=win.10)) ( https://msdn.microsoft.com/directx/aa937788.aspx) .

Aunque el ejemplo de instalador de D3D11InstallHelper que se describe en [implementación de Direct3D 11 para desarrolladores de juegos](../direct3darticles/direct3d11-deployment.md)se ha escrito para aplicaciones que usan Direct3D 11, proporciona un buen ejemplo de cómo interactuar con el [Windows Update API del agente](/windows/desktop/Wua_Sdk/portal-client) para iniciar y realizar un seguimiento de la descarga e instalación de actualizaciones que se hospedan en Windows Update. La compilación de este ejemplo puede requerir el Windows SDK para Windows 7. Para obtener información adicional sobre el ejemplo D3D11InstallHelper, incluidos los problemas conocidos, consulte el [SDK de DirectX](/previous-versions/windows/apps/hh452744(v=win.10)) ( https://msdn.microsoft.com/directx/aa937788.aspx) notas de la versión de agosto de 2009. actualización de la plataforma para Windows Vista)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Actualización de la plataforma para Windows Vista](platform-update-for-windows-vista-portal.md)
</dt> <dt>

**Temas de introducción**
</dt> <dt>

[Acerca de la actualización de la plataforma para Windows Vista](platform-update-for-windows-vista-overview.md)
</dt> <dt>

[Artículo de Knowledge Base acerca de la actualización de la plataforma para Windows Vista (KB 971644)](https://support.microsoft.com/kb/971644)
</dt> </dl>

 

 