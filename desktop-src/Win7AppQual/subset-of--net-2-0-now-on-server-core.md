---
description: Subconjunto de .NET 2.0 ahora en Server Core
ms.assetid: f91c4604-b2d6-41e5-be66-bbc8a4f0e28e
title: Subconjunto de .NET 2.0 ahora en Server Core
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b6ef839f525acf190df384e3fe8394f2b785d45
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116153"
---
# <a name="subset-of-net-20-now-on-server-core"></a>Subconjunto de .NET 2.0 ahora en Server Core

## <a name="platform"></a>Plataforma

**Servidores:** Windows Server 2008 R2  



## <a name="feature-impact"></a>Impacto en las características

 **Gravedad:** baja  
**Frecuencia:** baja  





## <a name="description"></a>Descripción

La opción de instalación Server Core para Windows Server 2008 R2 ahora incluye un subconjunto del .NET Framework 2.0. El subconjunto es la funcionalidad de .NET 2.0 que se alinea con la funcionalidad de Server Core. no se agregaron archivos binarios a la base de Server Core para permitir que ninguna parte de .NET 2.0 funcione.

No había compatibilidad con .NET en la opción de instalación Server Core para Windows Server 2008.

## <a name="manifestation-of-impact"></a>Demostración del impacto

Esto permite que algunas aplicaciones basadas en .NET 2.0 se ejecuten en Server Core en Windows Server 2008 R2.

## <a name="testing"></a>Prueba

Compruebe que las clases de .NET que usa el código están incluidas en Server Core. Pruebe también cualquier aplicación que ejecute este código en Server Core.

## <a name="links-to-other-resources"></a>Vínculos a otros recursos

-   [Server Core](/previous-versions/windows/desktop/legacy/ms723891(v=vs.85))
-   [Server Core Blog](https://blogs.technet.com/server_core/archive/2008/11/25/net-2-0-and-server-core-in-windows-server-2008-r2.aspx)
-   *Consulte también* la sección Server Core del *SDK de Windows Server 2008 R2* cuando esté disponible.

> [!Note]  
> Es posible que estos recursos no estén disponibles en algunos idiomas y países o regiones.

 

 

 
