---
title: Funciones llamadas por el sistema
description: Funciones llamadas por el sistema
ms.assetid: 006ac524-d456-44e9-957b-42a85dc92519
keywords:
- audio multimedia, funciones ACM
- audio, funciones ACM
- Administrador de compresión de audio (ACM), funciones
- ACM (Administrador de compresión de audio), funciones
- Funciones ACM
- funciones de devolución de llamada
- Administrador de compresión de audio (ACM), funciones de devolución de llamada
- ACM (Administrador de compresión de audio), funciones de devolución de llamada
- procedimientos de enlace
- procedimientos del controlador
- Administrador de compresión de audio (ACM), procedimientos de enlace
- ACM (Administrador de compresión de audio), procedimientos de enlace
- Administrador de compresión de audio (ACM), procedimientos de controlador
- ACM (Administrador de compresión de audio), procedimientos de controlador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1324ea168892d54f21754658607476c35075910
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "105651362"
---
# <a name="functions-called-by-the-system"></a>Funciones llamadas por el sistema

El sistema llama a tres tipos diferentes de funciones definidas por la aplicación. Las funciones de devolución de llamada son funciones de la aplicación a las que el sistema llama en respuesta a una solicitud realizada por una aplicación. Los procedimientos de enlace ayudan a una aplicación a controlar la personalización de los cuadros de diálogo. Un procedimiento de controlador es la implementación de una aplicación de su propio códec, convertidor o filtro.

Las funciones de devolución de llamada tienen los nombres siguientes:

-   [**acmDriverEnumCallback**](/windows/win32/api/msacm/nc-msacm-acmdriverenumcb)
-   [**acmFilterEnumCallback**](/windows/desktop/api/Msacm/nc-msacm-acmfilterenumcb)
-   [**acmFilterTagEnumCallback**](/windows/desktop/api/Msacm/nc-msacm-acmfiltertagenumcb)
-   [**acmFormatEnumCallback**](/windows/desktop/api/Msacm/nc-msacm-acmformatenumcb)
-   [**acmFormatTagEnumCallback**](/windows/desktop/api/Msacm/nc-msacm-acmformattagenumcb)
-   [**acmStreamConvertCallback**](/previous-versions//dd742925(v=vs.85))

La mayoría de las funciones de enumeración en ACM usan funciones de devolución de llamada. Por ejemplo, al llamar a una función de enumeración, el ACM enumera los elementos mediante una llamada repetida a la aplicación a través de la función de devolución de llamada.

No se puede llamar a algunas funciones desde estas funciones de devolución de llamada. Funciones a las que no se puede llamar manipular estructuras ACM internas usadas por las funciones de enumeración. No se debe llamar a las siguientes funciones desde una función de devolución de llamada:

-   [**acmDriverAdd**](/windows/desktop/api/Msacm/nf-msacm-acmdriveradd)
-   [**acmDriverPriority**](/windows/desktop/api/Msacm/nf-msacm-acmdriverpriority)
-   [**acmDriverRemove**](/windows/desktop/api/Msacm/nf-msacm-acmdriverremove)

El sistema llama a las siguientes funciones para ayudar a que una aplicación controle la personalización de los cuadros de diálogo:

-   [**acmFilterChooseHookProc**](/windows/desktop/api/Msacm/nc-msacm-acmfilterchoosehookproc)
-   [**acmFormatChooseHookProc**](/windows/desktop/api/Msacm/nc-msacm-acmformatchoosehookproc)

La función siguiente se especifica como un prototipo que permite a una aplicación usar un códec, convertidor o filtro personalizado. Una función que se ajuste a este prototipo se puede pasar como argumento a la función [**acmDriverAdd**](/windows/desktop/api/Msacm/nf-msacm-acmdriveradd) .

-   [**acmDriverProc**](/windows/desktop/api/Msacm/nc-msacm-acmdriverproc)

 

 