---
description: Un circular es una región delimitada por la intersección de una curva de elipse y dos radiales. En la ilustración siguiente se muestra un gráfico circular dibujado mediante la función Pie.
ms.assetid: 9ba7834e-02d2-4335-94c3-ab2f5c355619
title: Acerca de Pies
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e447e313a3088bbf9a72c790115fb3bb25770017cf13ce7922685fd18ccfe671
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119966465"
---
# <a name="about-pies"></a>Acerca de Pies

Un *circular* es una región delimitada por la intersección de una curva de elipse y dos radiales. En la ilustración siguiente se muestra un gráfico circular dibujado mediante la [**función Pie.**](/windows/desktop/api/Wingdi/nf-wingdi-pie)

![ilustración que muestra una elipse con un circular sombreado](images/csfsh-03.png)

Al llamar a [**Pie**](/windows/win32/api/wingdi/nf-wingdi-pie), una aplicación proporciona las coordenadas de las esquinas superior izquierda e inferior derecha del rectángulo delimitador de la elipse, así como las coordenadas de dos puntos que definen dos radiales.

Cuando el sistema dibuja la parte curva del gráfico circular, usa la dirección del arco actual para el contexto de dispositivo dado. La dirección de arco predeterminada es en sentido contrario a las agujas del reloj. Una aplicación puede restablecer la dirección del arco llamando a la [**función SetDirection.**](/windows/desktop/api/Wingdi/nf-wingdi-setarcdirection)

 

 
