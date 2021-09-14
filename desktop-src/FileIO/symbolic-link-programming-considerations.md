---
description: Consideraciones de programación para trabajar con vínculos simbólicos.
ms.assetid: 8966ac3e-a92b-4d68-b40b-e32a4173f869
title: Consideraciones de programación (sistemas de archivos locales)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a5d63c231c88da95efc0e5078506bf9fc0d6d9a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069835"
---
# <a name="programming-considerations-local-file-systems"></a>Consideraciones de programación (sistemas de archivos locales)

Tenga en cuenta las siguientes consideraciones de programación al trabajar con vínculos simbólicos:

-   Los vínculos simbólicos pueden apuntar a un destino inexistente.
-   Al crear un vínculo simbólico, el sistema operativo no comprueba si el destino existe.
-   Si una aplicación intenta abrir un destino inexistente, se devuelve **ERROR \_ FILE NOT \_ \_ FOUND.**
-   Los vínculos simbólicos son puntos de reanción. Para obtener más información, vea [Determinar si un directorio es una carpeta montada.](determining-whether-a-directory-is-a-volume-mount-point.md)
-   Hay un máximo de 63 puntos de reanción (y, por tanto, vínculos simbólicos) permitidos en una ruta de acceso determinada.

    **Windows Server 2003 y Windows XP:** Hay un límite de 31 puntos de reanción en cualquier ruta de acceso determinada.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>


</dt> <dt>

[Vínculos y uniones duros](hard-links-and-junctions.md)
</dt> </dl>

 

 



