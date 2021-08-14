---
description: Consideraciones de programación para trabajar con vínculos simbólicos.
ms.assetid: 8966ac3e-a92b-4d68-b40b-e32a4173f869
title: Consideraciones de programación (sistemas de archivos locales)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79a98c244dac3fb4a9f6b73d11067af64512e0cfd54e58078bd87a2582b0c2de
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119981885"
---
# <a name="programming-considerations-local-file-systems"></a>Consideraciones de programación (sistemas de archivos locales)

Tenga en cuenta las siguientes consideraciones de programación al trabajar con vínculos simbólicos:

-   Los vínculos simbólicos pueden apuntar a un destino inexistente.
-   Al crear un vínculo simbólico, el sistema operativo no comprueba si el destino existe.
-   Si una aplicación intenta abrir un destino inexistente, se devuelve **ERROR \_ FILE NOT \_ \_ FOUND.**
-   Los vínculos simbólicos son puntos de reanción. Para obtener más información, vea [Determinar si un directorio es una carpeta montada.](determining-whether-a-directory-is-a-volume-mount-point.md)
-   Hay un máximo de 63 puntos de reanbolso (y, por tanto, vínculos simbólicos) permitidos en una ruta de acceso determinada.

    **Windows Server 2003 y Windows XP:** Hay un límite de 31 puntos de rean aproximado en cualquier ruta de acceso determinada.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>


</dt> <dt>

[Vínculos duros y uniones](hard-links-and-junctions.md)
</dt> </dl>

 

 



