---
title: Tipos de compatibilidad con IAccessible
description: Tipos de compatibilidad con IAccessible
ms.assetid: 4a61d9a4-3c05-4f12-bdf1-426223b679b5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0fb38ed0b5f7a306f2551085c77f77a3793efec3bc9281cd44d1d7277abe81fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118993985"
---
# <a name="types-of-iaccessible-support"></a>Tipos de compatibilidad con IAccessible

Microsoft Active Accessibility servidores tienen dos tipos de compatibilidad [**con IAccessible:**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) nativa y con proxy. Los elementos de interfaz de usuario usados en una aplicación determinan qué tipo de compatibilidad es adecuada. Muchos servidores que se escriben hoy en día aprovechan al máximo los servidores proxy **IAccessible** y solo implementan **IAccessible** para los controles que no son proxy de Oleacc.dll, como controles sin ventanas o controles con un nombre de clase de ventana personalizado.

## <a name="in-this-section"></a>En esta sección

-   [Implementación Active Accessibility nativa](native-active-accessibility-implementation.md)
-   [Servidores proxy IAccessible](iaccessible-proxies.md)

 

 




