---
title: Tipos de compatibilidad de IAccessible
description: Tipos de compatibilidad de IAccessible
ms.assetid: 4a61d9a4-3c05-4f12-bdf1-426223b679b5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fb2cb3d25e4cf95cc1ad790c77ffe66e02efda2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103776224"
---
# <a name="types-of-iaccessible-support"></a>Tipos de compatibilidad de IAccessible

Los servidores de Microsoft Active Accessibility tienen dos tipos de compatibilidad con [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) : nativo y proxy. Los elementos de la interfaz de usuario usados en una aplicación determinan qué tipo de soporte técnico es adecuado. Muchos servidores que se escriben actualmente sacan el máximo partido de los proxies de **IAccessible** y solo implementan **IAccessible** para los controles que no son proxy de Oleacc.dll, como controles sin ventanas o controles con un nombre de clase de ventana personalizado.

## <a name="in-this-section"></a>En esta sección

-   [Implementación de Active Accessibility nativa](native-active-accessibility-implementation.md)
-   [Proxies de IAccessible](iaccessible-proxies.md)

 

 




