---
title: Convenciones de nomenclatura
description: Las convenciones de nomenclatura comparten un objetivo común para resolver de forma inequívoca un nombre en una dirección de red, generalmente una dirección IP. La diferencia entre las convenciones de nomenclatura radica en el enfoque distinto de cada Convención para resolver nombres.
ms.assetid: 1ec96d2d-bb5a-4938-88c2-4d2802a326cd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2091123ed2bf1022910231cd08cb0e6cccae51a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076007"
---
# <a name="naming-conventions"></a>Convenciones de nomenclatura

Las convenciones de nomenclatura comparten un objetivo común: para resolver de forma inequívoca un nombre en una dirección de red, generalmente una dirección IP. La diferencia entre las convenciones de nomenclatura radica en el enfoque distinto de cada Convención para resolver nombres.

Las convenciones de nomenclatura siguientes se usan para identificar equipos en varios métodos de resolución de nombres del sistema, incluido el método 2000 de Windows:

-   [Nombre del equipo](#computer-name)
-   [Nombre de host](#host-name)
-   [Nombre de dominio completo (FQDN)](#fully-qualified-domain-name)
-   [Nombre distintivo relativo](#relative-distinguished-name)

## <a name="computer-name"></a>Nombre del equipo

En el espacio de nombres NetBIOS sin formato, un nombre único resuelve de forma inequívoca un nombre de equipo en una dirección de red. Este es el nombre de las versiones anteriores de Windows que se almacenan en las listas del explorador y del explorador principal, lo que permite que las redes Windows del mismo nivel exploren los recursos en equipos Windows en red. En este escenario, el término asociado con el equipo era el *nombre del equipo*. El registro del nombre del equipo depende de las difusiones de red (y un explorador maestro, determinado por las elecciones logradas por los números de versión de Windows posteriores o el uso de Windows NT, o una combinación de ambos). Esto era útil para redes pequeñas de Windows basadas en el mismo nivel, pero las redes pronto crecieron más allá de lo que el uso de difusiones y las listas sencillas de exploradores maestros de archivos sin formato podrían servir.

## <a name="host-name"></a>Nombre de host

A continuación, llegó a Windows Internet Naming Service (WINS), que permitía un repositorio dinámico y centralizado de nombres de equipo basados en NetBIOS almacenados en servidores WINS. Estos repositorios podrían atender una red más grande. Con este desarrollo, las consultas de resolución de nombres pueden dirigirse a un servidor WINS (en lugar de difundirse) y los conflictos podrían ser arbitrados de forma centralizada. Con WINS, se reservó el término nombre del equipo, pero el término *nombre de host* también apareció y se usó indistintamente con el nombre de equipo. En ese momento, WINS era la resolución de nombres predeterminada para las plataformas de Windows, pero DNS estaba ganando la popularidad y la proliferación de redes grandes y mayores.

Las redes aumentaron y GANAban menos capaces de administrar el creciente volumen de nombres. La capacidad decreciente de WINS para controlar la carga de resolución de nombres no se debió a la potencia de procesamiento necesaria para la resolución, sino que, por el hecho de que generar nombres únicos para un gran número de equipos se convirtió en una carga de administración cada vez mayor.

## <a name="fully-qualified-domain-name"></a>Nombre de dominio completo

DNS es una solución mejor; con su espacio de nombres jerárquico, la necesidad de nombres de equipo únicos se aísla en un dominio determinado, lo que permite que un nombre de equipo como *server1* exista en ubicaciones de dominio diferentes en la misma jerarquía. Con la capacidad de tener el mismo nombre de host en dominios diferentes, la necesidad surgió para un nombre que se dirigió correctamente a la jerarquía de DNS. El nombre tenía que incluir no solo el nombre del equipo o el nombre de host, sino también un nombre que podría identificar de forma inequívoca, o calificar, ese equipo en toda la jerarquía de DNS. Ese nombre es el [*nombre de dominio completo*](f-gly.md) (FQDN), por ejemplo, server1.widgets.Microsoft.com.

Sin embargo, en determinadas situaciones, la parte de la jerarquía de dominios del FQDN es complicada y se necesita un nombre local para un equipo determinado (o cualquier otro host DNS) relacionado con el dominio DNS en el que reside el host. Ese nombre es el [*nombre distintivo relativo*](r-gly.md). El nombre distintivo relativo es simplemente el nombre de host único a la izquierda del punto situado más a la izquierda en el FQDN, de modo que un FQDN de server1.widgets.microsoft.com tiene server1 como su nombre distintivo relativo.

## <a name="relative-distinguished-name"></a>Nombre distintivo relativo

En lugar de imponer nuevos nombres o nuevas convenciones de nomenclatura para los usuarios de nombres NetBIOS, DNS simplemente usa el nombre de equipo (nombre de host) como nombre distintivo relativo y anexa la jerarquía de dominios DNS a ese nombre para crear el FQDN. En la ilustración siguiente se muestra cómo identificar la parte del nombre de equipo (o nombre de host o nombre distintivo relativo) del FQDN:

![combinación de la jerarquía de dominios de RDN y DNS para crear un FQDN](images/fqdn.png)

 

 




