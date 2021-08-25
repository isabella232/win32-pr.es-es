---
description: El controlador de dominio de información se usa para recuperar los datos predeterminados del dispositivo.
ms.assetid: 8fd05c17-e8c9-4747-9a66-ce7d958edeb9
title: Contextos de dispositivo de información
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 974b861f47ffbd19566a5224d0c2705e9797e86abbe46005c6eb1687a9573378
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119779135"
---
# <a name="information-device-contexts"></a>Contextos de dispositivo de información

El controlador de dominio de información se usa para recuperar los datos predeterminados del dispositivo. Por ejemplo, una aplicación puede llamar a la función [**CreateIC**](/windows/desktop/api/Wingdi/nf-wingdi-createica) para crear un controlador de dominio de información para un modelo determinado de impresora y, a continuación, llamar a las funciones [**GetCurrentObject**](/windows/desktop/api/Wingdi/nf-wingdi-getcurrentobject) y [**GetObject**](/windows/desktop/api/Wingdi/nf-wingdi-getobject) para recuperar los atributos de lápiz o pincel predeterminados. Dado que el sistema puede recuperar información del dispositivo sin crear las estructuras asociadas normalmente a los otros tipos de contextos de dispositivo, un controlador de dominio de información implica una sobrecarga mucho menor y se crea mucho más rápido que cualquiera de los otros tipos. Una vez que una aplicación termina de recuperar datos mediante un controlador de dominio de información, debe llamar a la [**función DeleteDC.**](/windows/desktop/api/Wingdi/nf-wingdi-deletedc)

 

 



