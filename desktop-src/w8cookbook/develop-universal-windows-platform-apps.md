---
title: Desarrollo de aplicaciones Windows plataforma universal (UWP)
description: Desarrollo de aplicaciones Windows plataforma universal (UWP)
ms.assetid: 215256D7-CBBA-43B0-A99C-490A25D1F82C
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b3654c1c8773a813fcc7f88b21a86c2ef6049184
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127574413"
---
# <a name="develop-universal-windows-platform-uwp-apps"></a>Desarrollo de aplicaciones Windows plataforma universal (UWP)

Animamos a todos los ISV de aplicaciones de escritorio (Win32) a que traigan sus aplicaciones de escritorio a la Plataforma universal de [Windows (UWP)](https://developer.microsoft.com/windows/bridges/desktop/) a través del Puente de dispositivo de escritorio. Las aplicaciones para UWP también se admiten en la [Tienda Windows](https://blogs.windows.com/buildingapps/2016/02/04/windows-store-trends-february-2016/), por lo que es más fácil actualizar automáticamente a los usuarios a una versión coherente, y esto reduce los costes de soporte técnico.

Si las aplicaciones de escritorio no se pueden convertir mediante el Puente de dispositivo de escritorio, se recomienda encarecidamente usar un instalador que siga los procedimientos recomendados y asegurarse de que está totalmente probado. Un instalador es la primera experiencia del usuario o cliente con la aplicación. Con demasiada frecuencia, el instalador no funciona correctamente o no se ha probado de forma completa en todos los escenarios. El Kit de certificación de aplicaciones de [Windows](https://dev.windows.com/develop/app-certification-kit) puede ayudarle a probar la instalación y desinstalación de la aplicación Win32 y a identificar el uso de API no documentadas, así como otros problemas básicos de procedimientos recomendados relacionados con el rendimiento antes que los usuarios.

## <a name="best-practices"></a>Procedimientos recomendados:

-   Usa instaladores que funcionen para versiones de Windows de 32 bits y de 64 bits.
-   Diseña tus instaladores para que funcionen en varios escenarios (en el nivel de usuario o de equipo).
-   Mantén todos los redistribuibles de Windows en el paquete original; si cambias el paquete, es posible que el instalador no funcione correctamente.
-   Programa el tiempo de desarrollo para tus instaladores, que a menudo se omiten como un entregable durante el ciclo de vida de desarrollo de software.

 

 




