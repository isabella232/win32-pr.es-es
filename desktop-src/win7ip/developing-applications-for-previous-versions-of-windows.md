---
title: Desarrollar aplicaciones para versiones anteriores de Windows
description: Explica qué hacer para desarrollar aplicaciones que se ejecutan en versiones anteriores de Windows y aprovechan las ventajas de la API que se admiten con la actualización de plataforma para Windows Vista y la actualización de plataforma para Windows Server 2008.
ms.assetid: 9c46f894-e5cd-46a1-81c8-f63b09504735
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7afbb999faf934ae621f80a824eca0289ff3df705ed11d7cfd161935c944947f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119549485"
---
# <a name="developing-applications-for-previous-versions-of-windows"></a>Desarrollar aplicaciones para versiones anteriores de Windows

Explica qué hacer para desarrollar aplicaciones que se ejecutan en versiones anteriores de Windows y aprovechan las ventajas de la API que se admiten con la actualización de plataforma para Windows Vista y la actualización de plataforma para Windows Server 2008.

## <a name="required-downloads"></a>Descargas necesarias

Es necesario descargar e instalar los paquetes que se describen en las secciones siguientes si desea desarrollar aplicaciones que usan api que se presentan con el Kit de desarrollo de software (SDK) de Microsoft Windows para Windows 7.

### <a name="microsoft-windows-sdk"></a>SDK de Windows Microsoft

El SDK de Windows para Windows 7 es necesario para crear aplicaciones que usan api compatibles con la actualización de plataforma para Windows Vista y la actualización de plataforma para Windows Server 2008.

Para obtener acceso a recursos e información adicionales, como descargas, publicaciones del foro y el blog del equipo del SDK de Windows, consulte el Centro para desarrolladores del SDK de [Windows](https://msdn.microsoft.com/bb980924.aspx) ( https://msdn.microsoft.com/bb980924.aspx) .

### <a name="net-framework"></a>.NET Framework

El .NET Framework 3.5 Service Pack 1 es necesario para crear aplicaciones que usan las API compatibles con la actualización de plataforma para Windows Vista y la actualización de plataforma para Windows Server 2008.

Para obtener información y recursos adicionales, [consulte el Centro .NET Framework desarrolladores](https://msdn.microsoft.com/netframework/default.aspx) ( https://msdn.microsoft.com/netframework/default.aspx) .

### <a name="directx-sdk-required-when-using-direct3d"></a>Sdk de DirectX necesario al usar Direct3D

Si crea aplicaciones que usan Direct3D, el SDK de [DirectX](/previous-versions/windows/apps/hh452744(v=win.10)) ( es necesario para crear aplicaciones que usan las API compatibles con la actualización de plataforma para Windows Vista y la actualización de plataforma https://msdn.microsoft.com/directx/aa937788.aspx) para Windows Server 2008.

### <a name="update-your-development-computer"></a>Actualización del equipo de desarrollo

Asegúrese de que el equipo de desarrollo tiene todas las actualizaciones más recientes de Windows Update.

Si está desarrollando aplicaciones en una versión anterior de Windows, debe obtener la actualización de plataforma para Windows Vista o la actualización de plataforma para Windows Server 2008 de Windows Update. La instalación de cualquiera de estas actualizaciones le permitirá aprovechar las ventajas de la nueva API proporcionada por el SDK de Windows para Windows 7.

Para obtener más información sobre cómo obtener actualizaciones de Windows Update, consulte el artículo de Knowledge Base sobre la actualización de plataforma para [Windows Vista (KB 971644)](https://support.microsoft.com/kb/971644) ( https://support.microsoft.com/kb/971644) .

## <a name="development-environment"></a>Entorno de desarrollo

### <a name="set-the-build-target-to-windows-7"></a>Establecer el destino de compilación en Windows 7

Todas las aplicaciones que usan bibliotecas en La actualización de plataforma para Windows Vista deben crearse en la Windows de destino 7.

Establecer WINVER en el valor de la plataforma de destino Windows 7 le permite desarrollar aplicaciones que usan api compatibles con la actualización de plataforma para Windows Vista o la actualización de plataforma para Windows Server 2008 en una máquina de desarrollo que ejecuta Windows Vista.

Puede establecer la plataforma de destino para Windows 7 en el código fuente o mediante la opción /D con el compilador Visual Studio.

En el ejemplo siguiente se muestra cómo establecer WINVER en el código fuente.


```C++
#define WINVER 0x0601
```



En el ejemplo siguiente se muestra cómo establecer WINVER mediante la opción del compilador /D.

``` syntax
/DWINVER=0x0601
```

## <a name="application-deployment"></a>Implementación de aplicaciones

Si compila la aplicación con los encabezados y bibliotecas proporcionados por el SDK de Windows para Windows 7, las API admitidas se ejecutarán en cualquier versión de Windows que tenga instalada la actualización de plataforma para Windows Vista o la actualización de plataforma para Windows Server 2008.

> [!Note]  
> El comportamiento, el rendimiento o los requisitos de algunas API compatibles con la actualización de plataforma para Windows Vista o la actualización de plataforma para Windows Server 2008 pueden variar en las distintas versiones de Windows. Para obtener más información sobre una API específica compatible con las actualizaciones, consulte Acerca de la actualización de plataforma [para Windows Vista](platform-update-for-windows-vista-overview.md).

 

### <a name="no-redistributable-components"></a>Sin componentes redistribuibles

La aplicación no necesita instalar componentes redistribuibles, como archivos DLL u otros archivos en tiempo de ejecución.

### <a name="requires-updated-end-user-computer"></a>Requiere actualizar End-User equipo

Dado que la actualización de plataforma para Windows Vista y la actualización de plataforma para Windows Server 2008 se hospedan en Windows Update, es muy probable que los usuarios finales con actualizaciones automáticas habilitadas ya tengan estas actualizaciones, así como los Service Pack necesarios.

Si el equipo del usuario final no tiene instalada la actualización de plataforma para Windows Vista o la actualización de plataforma para Windows Server 2008 y la aplicación requiere API compatibles con estas actualizaciones, es posible que la aplicación no pueda ejecutarse en el equipo del usuario final o que se encuentren errores durante la ejecución.

Para evitar los problemas que podrían deberse a que el equipo del usuario no está actualizado, quiere comprobar que el equipo del usuario tiene la actualización de plataforma para Windows Vista o la actualización de plataforma para Windows Server 2008 durante la instalación de la aplicación. Puede usar la API [Windows Update Agent para](/windows/desktop/Wua_Sdk/portal-client) comprobar si hay actualizaciones instaladas en el equipo del usuario final. También puede usar la API Windows Update Agent para descargar e instalar las actualizaciones necesarias durante la instalación de la aplicación si el usuario final aún no ha instalado las actualizaciones.

Para obtener un ejemplo de un instalador que muestra cómo usar la API del agente de actualización de [Windows](/windows/desktop/Wua_Sdk/portal-client), vea Implementación de [Direct3D 11](../direct3darticles/direct3d11-deployment.md) para desarrolladores de juegos en el [SDK de DirectX](/previous-versions/windows/apps/hh452744(v=win.10)) ( https://msdn.microsoft.com/directx/aa937788.aspx) .

Aunque el ejemplo del instalador D3D11InstallHelper que se describe en Implementación de [Direct3D 11](../direct3darticles/direct3d11-deployment.md)para desarrolladores de juegos, se escribió para aplicaciones que usan Direct3D 11, proporciona un buen ejemplo de cómo interactuar con la API del agente de actualización de [Windows](/windows/desktop/Wua_Sdk/portal-client) para iniciar y realizar un seguimiento de la descarga e instalación de actualizaciones hospedadas por Windows Update. La compilación de este ejemplo puede requerir el SDK Windows para Windows 7. Para obtener información adicional sobre el ejemplo D3D11InstallHelper, incluidos los problemas conocidos, consulte el [SDK de DirectX](/previous-versions/windows/apps/hh452744(v=win.10)) (Notas de la versión de agosto de https://msdn.microsoft.com/directx/aa937788.aspx) 2009.Platform Update for Windows Vista).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Actualización de plataforma para Windows Vista](platform-update-for-windows-vista-portal.md)
</dt> <dt>

**Temas de introducción**
</dt> <dt>

[Acerca de la actualización de plataforma para Windows Vista](platform-update-for-windows-vista-overview.md)
</dt> <dt>

[Knowledge Base sobre la actualización de plataforma para Windows Vista (KB 971644)](https://support.microsoft.com/kb/971644)
</dt> </dl>

 

 