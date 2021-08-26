---
description: Identificación de operaciones de DVD válidas
ms.assetid: d368b552-7ed3-4334-b97b-ff49d6c331c3
title: Identificación de operaciones de DVD válidas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fd1b99a38949ca0ff54d391e9ad5458bbe854a5c4af4140b15deaf4177147aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120051985"
---
# <a name="identifying-valid-dvd-operations"></a>Identificación de operaciones de DVD válidas

Varios factores determinan si puede realizar una operación de DVD determinada:

-   Dominio actual. Algunos comandos solo son válidos en determinados dominios. Cuando cambia el dominio, el navegador envía un evento EC \_ DVD \_ DOMAIN \_ CHANGE. También puede llamar a [**IDvdInfo2::GetCurrentDomain**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getcurrentdomain) para obtener el dominio actual.
-   Marcas de UOPS. Se trata de marcas escritas en el disco que indican qué operaciones se permiten. Cada vez que cambian las marcas, el navegador envía un evento \_ EC DVD \_ VALID \_ UOPS CHANGE con las nuevas \_ marcas. También puede llamar a [**IDvdInfo2::GetCurrentUOPS para**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getcurrentuops) obtener las marcas de UOPS actuales.
-   Contenido de DVD. Es posible que algunos comandos no sean pertinentes en función del contenido del DVD. Por ejemplo, el método [**IDvdControl2::SelectAngle**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectangle) podría permitirse según el dominio actual y las marcas de UOPS, pero el vídeo podría tener solo un ángulo. En ese caso, se permite la llamada **SelectAngle,** pero no es una opción significativa.

Cuando esté en duda, permita una acción. En el peor de los casos, se producirá un error en el [**método IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) y puede enviar comentarios al usuario. Los comentarios deben ser relativamente discretos. Por ejemplo, podría parpadear una pequeña X roja para alertar al usuario. El navegador de DVD devuelve VFW E DVD INVALIDDOMAIN cuando el dominio prohíbe una operación \_ \_ y \_ VFW E DVD OPERATION PROHIBITED cuando las marcas de UOPS prohíben \_ \_ una \_ \_ operación.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Aplicaciones de DVD](dvd-applications.md)
</dt> </dl>

 

 



