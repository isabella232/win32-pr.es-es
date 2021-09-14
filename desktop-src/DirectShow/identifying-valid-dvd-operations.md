---
description: Identificación de operaciones de DVD válidas
ms.assetid: d368b552-7ed3-4334-b97b-ff49d6c331c3
title: Identificación de operaciones de DVD válidas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 444595e402dc73a3468946b820f031dabaecc2f2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127072174"
---
# <a name="identifying-valid-dvd-operations"></a>Identificación de operaciones de DVD válidas

Varios factores determinan si puede realizar una operación de DVD determinada:

-   Dominio actual. Algunos comandos solo son válidos en determinados dominios. Cuando cambia el dominio, el navegador envía un evento EC \_ DVD \_ DOMAIN \_ CHANGE. También puede llamar a [**IDvdInfo2::GetCurrentDomain**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getcurrentdomain) para obtener el dominio actual.
-   Marcas de UOPS. Se trata de marcas escritas en el disco que indican qué operaciones se permiten. Cada vez que cambian las marcas, el navegador envía un evento \_ EC DVD \_ VALID \_ UOPS CHANGE con las nuevas \_ marcas. También puede llamar a [**IDvdInfo2::GetCurrentUOPS para**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getcurrentuops) obtener las marcas de UOPS actuales.
-   Contenido de DVD. Es posible que algunos comandos no sean pertinentes en función del contenido del DVD. Por ejemplo, el método [**IDvdControl2::SelectAngle**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectangle) podría permitirse según el dominio actual y las marcas de UOPS, pero el vídeo podría tener solo un ángulo. En ese caso, se permite la llamada **SelectAngle,** pero no es una opción significativa.

Cuando esté en duda, permita una acción. En el peor de los casos, se producirá un error en el método [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) y puede enviar comentarios al usuario. Los comentarios deben ser relativamente discretos. Por ejemplo, podría parpadear una pequeña X roja para alertar al usuario. El navegador de DVD devuelve VFW E DVD INVALIDDOMAIN cuando el dominio prohíbe una operación, y VFW E DVD OPERATION ESTANDO PROHIBIDO CUANDO las marcas \_ \_ de \_ \_ \_ \_ \_ UOPS prohíben una operación.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Aplicaciones de DVD](dvd-applications.md)
</dt> </dl>

 

 



