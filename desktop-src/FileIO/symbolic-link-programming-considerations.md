---
description: Consideraciones de programación para trabajar con vínculos simbólicos.
ms.assetid: 8966ac3e-a92b-4d68-b40b-e32a4173f869
title: Consideraciones de programación (sistemas de archivos locales)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a5d63c231c88da95efc0e5078506bf9fc0d6d9a
ms.sourcegitcommit: 3d9dce1bd6c84e2b51759e940aa95aa9b459cd20
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/04/2021
ms.locfileid: "105689682"
---
# <a name="programming-considerations-local-file-systems"></a>Consideraciones de programación (sistemas de archivos locales)

Tenga en cuenta las siguientes consideraciones de programación al trabajar con vínculos simbólicos:

-   Los vínculos simbólicos pueden apuntar a un destino no existente.
-   Al crear un vínculo simbólico, el sistema operativo no comprueba si existe el destino.
-   Si una aplicación intenta abrir un destino no existente, se devuelve **el \_ archivo de error \_ no \_ encontrado** .
-   Los vínculos simbólicos son puntos de reanálisis. Para obtener más información, vea [determinar si un directorio es una carpeta montada](determining-whether-a-directory-is-a-volume-mount-point.md).
-   Hay un máximo de 63 puntos de análisis (y, por lo tanto, vínculos simbólicos) permitidos en una ruta de acceso determinada.

    **Windows Server 2003 y Windows XP:** Hay un límite de 31 puntos de análisis en una ruta de acceso dada.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>


</dt> <dt>

[Vínculos físicos y uniones](hard-links-and-junctions.md)
</dt> </dl>

 

 



