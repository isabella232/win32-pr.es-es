---
description: Uso .NET Framework 4 con aplicaciones creadas en versiones anteriores
ms.assetid: 287E25AD-A560-40DA-A4E6-C46A3123914E
title: Uso .NET Framework 4 con aplicaciones creadas en versiones anteriores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a12eb34b00cfe14a18e83e7726f1ffa962ba03f8
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122884744"
---
# <a name="using-net-framework-4-with-applications-built-on-earlier-versions"></a>Uso .NET Framework 4 con aplicaciones creadas en versiones anteriores

## <a name="platform"></a>Plataforma

 **Clientes:** Windows XP, Windows Vista, Windows 7  
**Servidores:** Windows Server 2003, Windows Server 2008, Windows Server 2008 R2  


## <a name="feature-impact"></a>Impacto en las características

 **Gravedad:** baja  
**Frecuencia:** alta  






## <a name="description"></a>Descripción

El .NET Framework 4 es altamente compatible con las aplicaciones que se han creado mediante versiones .NET Framework anteriores. Los cambios principales en .NET Framework 4 son mejorar la seguridad, el cumplimiento de estándares, la corrección, la confiabilidad y el rendimiento.

Sin embargo, .NET Framework 4 no usa automáticamente su versión de Common Language Runtime (CLR) para ejecutar aplicaciones compiladas mediante versiones anteriores del .NET Framework.

## <a name="manifestation"></a>Manifestación

Si ha creado una aplicación mediante un .NET Framework anterior y un usuario abre esa aplicación en un equipo que tiene instalado .NET Framework 4 y la versión anterior de .NET Framework, la aplicación usa la versión anterior de CLR.

Sin embargo, si .NET Framework 4 es la única versión en tiempo de ejecución instalada en el equipo, la aplicación produce una excepción y pide al usuario que instale la versión en tiempo de ejecución en la que ha creado la aplicación.

## <a name="solution"></a>Solución

Para ejecutar aplicaciones compiladas con versiones anteriores de .NET Framework con .NET Framework 4, debe compilar la aplicación para que la versión .NET Framework 4 se especifique en las propiedades del proyecto en Microsoft Visual Studio, o bien puede especificar .NET Framework 4 en el elemento [**&lt; supportedRuntime &gt;**](/previous-versions/dotnet/netframework-1.1/w4atty68(v=vs.71)) en un archivo de configuración de la aplicación.

Para obtener más información sobre cómo migrar a la versión .NET Framework 4, vea Migration Guide to the .NET Framework 4 (Guía de migración a [.NET Framework 4)](/previous-versions/dotnet/netframework-4.0/ff657133(v=vs.100)) y [Version Compatibility (Compatibilidad](/previous-versions/dotnet/netframework-4.0/ff602939(v=vs.100))de versiones) .NET Framework .

## <a name="compatibility-tests"></a>Pruebas de compatibilidad

Después de realizar los cambios, pruebe la aplicación para asegurarse de que se ejecuta correctamente. Puede probar la compatibilidad como se describe en el [.NET Framework compatibilidad de aplicaciones 4.](/previous-versions/dd889541(v=msdn.10))

Si la aplicación o componente no funciona después de .NET Framework 4 está instalado, envíe un error a través del sitio [web Conectar Microsoft.](https://connect.microsoft.com/visualstudio)

## <a name="links-to-other-resources"></a>Vínculos a otros recursos

-   [**&lt;elemento &gt; supportedRuntime**](/previous-versions/dotnet/netframework-1.1/w4atty68(v=vs.71))
-   [Guía de migración para .NET Framework 4](/previous-versions/dotnet/netframework-4.0/ff657133(v=vs.100))
-   [Compatibilidad de versiones en .NET Framework](/previous-versions/dotnet/netframework-4.0/ff602939(v=vs.100))
-   **.NET Framework tutorial de compatibilidad de aplicaciones 4 RTM:**<https://msdn.microsoft.com/library/dd889541.aspx>
-   [Microsoft Connect](https://connect.microsoft.com/)

 

 
