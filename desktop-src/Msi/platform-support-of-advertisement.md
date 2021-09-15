---
description: El instalador Windows admite anuncios de aplicaciones y características.
ms.assetid: 9e5158bc-4877-49d1-9bb9-4dd17abb444d
title: Compatibilidad de la plataforma con anuncios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48016241998473a5bb5ae8ecff05a14fd702f8be
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127473964"
---
# <a name="platform-support-of-advertisement"></a>Compatibilidad de la plataforma con anuncios

El instalador Windows admite anuncios de aplicaciones y características.

Las siguientes funcionalidades de anuncio están disponibles en Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003, Windows XP y Windows 2000.

-   Accesos directos y sus iconos.

-   Extensiones y sus iconos especificados en la [tabla ProgId](progid-table.md).

-   Verbos de shell y comando registrados debajo de la clave ProgId.

-   Contextos CLSID e InProcHandler.

-   Install-On-Demand a través de OLE solo está disponible mediante programación a través de [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) (C/C++) y la función **CreateObject (Visual Basic)** u **GetObject (Visual Basic).**

> [!Note]
> La información de AppId y Typelib solo se escribe cuando se instala un componente anunciado.
> 
> Para admitir extensiones de nombre de archivo, un administrador debe publicar la aplicación en Active Directory mediante directiva de grupo.

## <a name="remarks"></a>Observaciones

Es posible que la instalación del producto no requiera un reinicio, pero los accesos directos anunciados no funcionarán hasta que se reinicie la máquina. Los accesos directos anunciados de las instalaciones posteriores funcionan sin reiniciar.

Para asegurarse de que los accesos directos anunciados funcionan correctamente, el autor del paquete debe programar un reinicio forzado al final de la instalación.

Para evitar reinicios innecesarios del sistema, programe un reinicio para que se ejecute solo si no hay ninguna versión del Windows instalado.

Las instrucciones condicionales pueden comprobar la [**propiedad ShellAdvtSupport**](shelladvtsupport.md) y [**la propiedad Version9X.**](version9x.md) Para obtener más información sobre cómo programar reinicios forzados condicionales, vea [Reinicios del](system-reboots.md) sistema y Uso de [propiedades en instrucciones condicionales](using-properties-in-conditional-statements.md).

 

 
