---
description: Usar .NET Framework 4 con aplicaciones creadas en versiones anteriores
ms.assetid: 287E25AD-A560-40DA-A4E6-C46A3123914E
title: Usar .NET Framework 4 con aplicaciones creadas en versiones anteriores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ef252d128ae5d3c8f5b85ef486828fb82e152d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707495"
---
# <a name="using-net-framework-4-with-applications-built-on-earlier-versions"></a>Usar .NET Framework 4 con aplicaciones creadas en versiones anteriores

## <a name="platform"></a>Plataforma

 **Clientes** -Windows XP Windows \| vista Windows \| 7  
**Servidores** : windows Server 2003 \| Windows Server 2008 \| Windows Server 2008 R2  


## <a name="feature-impact"></a>Impacto en las características

 **Gravedad** baja  
**Frecuencia** : alta  






## <a name="description"></a>Descripción

El .NET Framework 4 es muy compatible con las aplicaciones compiladas con versiones anteriores de .NET Framework. Los principales cambios en .NET Framework 4 son para mejorar la seguridad, el cumplimiento de estándares, la corrección, la confiabilidad y el rendimiento.

Sin embargo, .NET Framework 4 no utiliza automáticamente su versión de Common Language Runtime (CLR) para ejecutar aplicaciones compiladas con versiones anteriores de la .NET Framework.

## <a name="manifestation"></a>Manifestación

Si ha creado una aplicación con una .NET Framework anterior y un usuario abre la aplicación en un equipo que tiene .NET Framework 4 y la versión anterior del .NET Framework instalado, la aplicación usa la versión anterior de CLR.

Sin embargo, si el .NET Framework 4 es la única versión en tiempo de ejecución instalada en el equipo, la aplicación produce una excepción y pide al usuario que instale la versión de tiempo de ejecución con la que compiló la aplicación.

## <a name="solution"></a>Solución

Para ejecutar aplicaciones que se compilan con versiones anteriores de .NET Framework con .NET Framework 4, debe compilar la aplicación para que tenga como destino la versión de .NET Framework 4 Si la especifica en las propiedades del proyecto en Microsoft Visual Studio, o puede especificar .NET Framework 4 en el [**<supportedRuntime> elemento**](/previous-versions/dotnet/netframework-1.1/w4atty68(v=vs.71)) de un archivo de configuración de la aplicación.

Para obtener más información sobre cómo migrar a la .NET Framework 4, vea [Guía de migración para la compatibilidad con .NET Framework 4](/previous-versions/dotnet/netframework-4.0/ff657133(v=vs.100)) y [versiones en el .NET Framework](/previous-versions/dotnet/netframework-4.0/ff602939(v=vs.100)).

## <a name="compatibility-tests"></a>Pruebas de compatibilidad

Después de realizar los cambios, pruebe la aplicación para asegurarse de que se ejecuta correctamente. Puede probar la compatibilidad como se describe en el tema de [compatibilidad de aplicaciones de .NET Framework 4](/previous-versions/dd889541(v=msdn.10)) .

Si su aplicación o componente no funciona después de instalar .NET Framework 4, envíe un error a través del sitio web de [Microsoft Connect](https://connect.microsoft.com/visualstudio) .

## <a name="links-to-other-resources"></a>Vínculos a otros recursos

-   [**<supportedRuntime> Element**](/previous-versions/dotnet/netframework-1.1/w4atty68(v=vs.71))
-   [Guía de migración para .NET Framework 4](/previous-versions/dotnet/netframework-4.0/ff657133(v=vs.100))
-   [Compatibilidad de versiones en .NET Framework](/previous-versions/dotnet/netframework-4.0/ff602939(v=vs.100))
-   **Tutorial de compatibilidad de aplicaciones de .NET Framework 4 RTM:**<https://msdn.microsoft.com/library/dd889541.aspx>
-   [Microsoft Connect](https://connect.microsoft.com/)

 

 
