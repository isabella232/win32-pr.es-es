---
title: Mensajes comunicados a través de interfaces de usuario
description: En este tema se enumeran los mensajes que un servicio de directorio puede enviar desde una interfaz de usuario.
ms.assetid: c81a3c44-c01d-4029-8a7d-6e0911d4f5ab
ms.tgt_platform: multiple
keywords:
- Mensajes comunicados a través de interfaces de usuario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b20b2706ae9f03109064c459ce494fb38da3f4579ca8f5b03ade970fcb0391f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118186588"
---
# <a name="messages-communicated-through-user-interfaces"></a>Mensajes comunicados a través de interfaces de usuario

En este tema se enumeran los mensajes que un servicio de directorio puede enviar desde una interfaz de usuario.

## <a name="common-query-page-messages"></a>Mensajes comunes de la página de consulta

Los mensajes siguientes se envían a una página de extensión de formulario de consulta de servicio de directorio en la función de devolución de llamada [**CQPageProc:**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc)

-   [**CQPM \_ CLEARFORM**](cqpm-clearform.md)
-   [**CQPM \_ ENABLE**](cqpm-enable.md)
-   [**CQPM \_ GETPARAMETERS**](cqpm-getparameters.md)
-   [**CQPM \_ HANDLERSPECIFIC**](cqpm-handlerspecific.md)
-   [**CQPM \_ HELP**](cqpm-help.md)
-   [**INICIALIZACIÓN DE CQPM \_**](cqpm-initialize.md)
-   [**CQPM \_ PERSIST**](cqpm-persist.md)
-   [**CQPM \_ RELEASE**](cqpm-release.md)
-   [**CQPM \_ SETDEFAULTPARAMETERS**](cqpm-setdefaultparameters.md)

## <a name="miscellaneous-messages"></a>Mensajes varios

En la tabla siguiente se enumeran los mensajes que un servicio de directorio puede enviar.



| Message                  | Valor                     | Descripción                                                                                                                                                                                                                                   |
|--------------------------|---------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DSPROP \_ ATTRCHANGED \_ MSG | "DsPropAttrChanged"       | Mensaje enviado para sincronizar páginas de propiedades y las herramientas de administración del servicio de directorio, declarado en Dsclient.h.                                                                                                                       |
| DSQPM \_ GETCLASSLIST      | CQPM \_ HANDLERSPECIFIC+0   | Mensaje de página enviado a las páginas del formulario para recuperar una lista de clases para la consulta, utilizada por el selector de campos y la propiedad well para crear su lista de clases para mostrar. wParam = flags y lParam = LPLPDSQUERYCLASSLIST, declarados en Dsquery.h. |
| TEMAS DE AYUDA DE DSQPM \_        | (CQPM) \_ HANDLERSPECIFIC+1) | Mensaje de página enviado a las páginas del formulario para controlar la solicitud "Temas de Ayuda". wParam = 0, lParam = hWndParent, declarado en Dsquery.h.                                                                                                         |



 

 

 




