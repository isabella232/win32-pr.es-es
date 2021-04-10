---
title: Mensajes que se comunican a través de interfaces de usuario
description: En este tema se enumeran los mensajes que un servicio de directorio puede enviar desde una interfaz de usuario.
ms.assetid: c81a3c44-c01d-4029-8a7d-6e0911d4f5ab
ms.tgt_platform: multiple
keywords:
- Mensajes que se comunican a través de interfaces de usuario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ab0d01717129db284f05b2361b2a067d611a33e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075116"
---
# <a name="messages-communicated-through-user-interfaces"></a>Mensajes que se comunican a través de interfaces de usuario

En este tema se enumeran los mensajes que un servicio de directorio puede enviar desde una interfaz de usuario.

## <a name="common-query-page-messages"></a>Mensajes de página de consulta comunes

Los siguientes mensajes se envían a una página de extensión de formulario de consulta de servicio de directorio en la función de devolución de llamada [**CQPageProc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc) :

-   [**CQPM \_ CLEARFORM**](cqpm-clearform.md)
-   [**\_habilitación de CQPM**](cqpm-enable.md)
-   [**CQPM \_ GETPARAMETERS**](cqpm-getparameters.md)
-   [**CQPM \_ HANDLERSPECIFIC**](cqpm-handlerspecific.md)
-   [**ayuda de CQPM \_**](cqpm-help.md)
-   [**CQPM \_ inicializar**](cqpm-initialize.md)
-   [**CQPM \_ Persist**](cqpm-persist.md)
-   [**versión de CQPM \_**](cqpm-release.md)
-   [**CQPM \_ SETDEFAULTPARAMETERS**](cqpm-setdefaultparameters.md)

## <a name="miscellaneous-messages"></a>Mensajes varios

En la tabla siguiente se enumeran los mensajes que puede enviar un servicio de directorio.



| Message                  | Value                     | Descripción                                                                                                                                                                                                                                   |
|--------------------------|---------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ATTRCHANGED de DSPROP \_ \_ | "DsPropAttrChanged"       | Mensaje enviado para sincronizar las páginas de propiedades y las herramientas de administración del servicio de directorio, declaradas en DSClient. h.                                                                                                                       |
| DSQPM \_ GETCLASSLIST      | CQPM \_ HANDLERSPECIFIC + 0   | Un mensaje de página enviado a las páginas del formulario para recuperar una lista de clases para la consulta, utilizada por el selector de campos y la propiedad bien para generar la lista de clases para mostrar. wParam = Flags e lParam = LPLPDSQUERYCLASSLIST, declarado en dsquery. h. |
| DSQPM \_ HELPTOPICS        | (CQPM \_ HANDLERSPECIFIC + 1) | Un mensaje de página enviado a las páginas del formulario para controlar la solicitud de "temas de ayuda". wParam = 0, lParam = hWndParent, declarado en dsquery. h.                                                                                                         |



 

 

 




