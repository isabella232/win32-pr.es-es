---
description: Identificación de las operaciones de DVD válidas
ms.assetid: d368b552-7ed3-4334-b97b-ff49d6c331c3
title: Identificación de las operaciones de DVD válidas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 444595e402dc73a3468946b820f031dabaecc2f2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104423036"
---
# <a name="identifying-valid-dvd-operations"></a>Identificación de las operaciones de DVD válidas

Algunos factores determinan si se puede realizar una operación de DVD determinada:

-   Dominio actual. Algunos comandos solo son válidos en determinados dominios. Cuando el dominio cambia, el navegador envía un evento de cambio de dominio de DVD de EC \_ \_ \_ . También puede llamar a [**IDvdInfo2:: GetCurrentDomain**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getcurrentdomain) para obtener el dominio actual.
-   Marcas de UOPS. Se trata de marcas escritas en el disco que indican qué operaciones se permiten. Cada vez que cambian las marcas, el navegador envía \_ un \_ \_ evento de cambio UOPS válido de un DVD \_ con las nuevas marcas. También puede llamar a [**IDvdInfo2:: GetCurrentUOPS**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getcurrentuops) para obtener las marcas UOPS actuales.
-   Contenido del DVD. Es posible que algunos comandos no sean relevantes en función del contenido del DVD. Por ejemplo, el método [**IDvdControl2:: SelectAngle**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectangle) podría estar permitido según el dominio actual y las marcas UOPS, pero el vídeo puede tener solo un ángulo. En ese caso, se permite la llamada **SelectAngle** , pero no es una opción significativa.

En casos de duda, permita una acción. En el peor de los demás, se producirá un error en el método [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) y podrá enviar comentarios al usuario. Los comentarios deben ser relativamente discretos. Por ejemplo, puede que parpadee una X roja pequeña para alertar al usuario. El navegador de DVD devuelve VFW \_ e \_ DVD \_ invaliddomain le cuando el dominio prohíbe una operación y \_ la operación VFW e \_ DVD se \_ \_ impide cuando las marcas de UOPS prohíben una operación.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Aplicaciones de DVD](dvd-applications.md)
</dt> </dl>

 

 



