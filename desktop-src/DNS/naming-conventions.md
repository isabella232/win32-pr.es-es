---
title: Convenciones de nomenclatura
description: Las convenciones de nomenclatura comparten un objetivo común para resolver de forma inequívoca un nombre en una dirección de red, generalmente una dirección IP. La diferencia entre las convenciones de nomenclatura radica en el enfoque distinto de cada convención para resolver nombres.
ms.assetid: 1ec96d2d-bb5a-4938-88c2-4d2802a326cd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9b378f9383f773cb24fb47c81cb92a066094a4ce528d7f3710212c6bb7cac0d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119076598"
---
# <a name="naming-conventions"></a>Convenciones de nomenclatura

Las convenciones de nomenclatura comparten un objetivo común: resolver de forma inequívoca un nombre en una dirección de red, generalmente una dirección IP. La diferencia entre las convenciones de nomenclatura radica en el enfoque distinto de cada convención para resolver nombres.

Las siguientes convenciones de nomenclatura se usan para identificar equipos en varios métodos de resolución de nombres del sistema, incluido el método Windows 2000:

-   [Nombre del equipo](#computer-name)
-   [Nombre de host](#host-name)
-   [Nombre de dominio completo (FQDN)](#fully-qualified-domain-name)
-   [Nombre distintivo relativo](#relative-distinguished-name)

## <a name="computer-name"></a>Nombre del equipo

En el espacio de nombres NetBIOS plano, un nombre único resuelve de forma inequívoca un nombre de equipo en una dirección de red. Este es el nombre que las versiones anteriores Windows almacenadas en listas de exploradores y exploradores maestros, lo que permite que las redes de Windows del mismo nivel examinen los recursos en Windows equipos. En este escenario, el término asociado al equipo era *nombre de equipo*. El registro del nombre del equipo dependía de las difusión de red (y de un explorador maestro, determinado por las elecciones ganadas por los números de versión de Windows posteriores o el uso Windows NT, o una combinación). Esto resultaba útil para redes pequeñas basadas en Windows del mismo nivel, pero las redes pronto creciendo más allá de lo que podía servir el uso de difusiones y listas de exploradores maestras de archivos planos simples.

## <a name="host-name"></a>Nombre de host

A continuación, Windows internet Naming Service (WINS), que habilita un repositorio dinámico y centralizado de nombres de equipos basados en NetBIOS almacenados en servidores WINS. Estos repositorios podrían dar servicio a una red más grande. Con este desarrollo, las consultas de resolución de nombres podrían dirigirse a un servidor WINS (en lugar de difundirse) y los conflictos se podrían resolver de forma centralizada. Con WINS, se conservaba el término nombre de equipo, pero el término *nombre de host* también aparecía y se usaba indistintamente con el nombre de equipo. En ese momento, WINS era el solucionador de nombres predeterminado para las plataformas Windows, pero DNS ganaba con la popularidad y proliferación de redes más grandes y grandes.

Las redes creciendo y WINS empezó a ser menos capaz de controlar el volumen creciente de nombres. La capacidad decreciente de WINS para controlar la carga de resolución de nombres no se debía a la capacidad de procesamiento necesaria para la resolución, sino al hecho de que la generación de nombres únicos para muchos equipos se convirtió en una carga de administración cada vez mayor.

## <a name="fully-qualified-domain-name"></a>Nombre de dominio completo

DNS es una solución mejor; con su espacio jerárquico de nombres, la necesidad de nombres de equipo únicos está aislada en un dominio determinado, lo que permite que un nombre de equipo como *server1* exista en diferentes ubicaciones de dominio de la misma jerarquía. Con la capacidad de tener el mismo nombre de host en dominios diferentes, se produjo la necesidad de un nombre que abordara correctamente la jerarquía DNS. El nombre tenía que incluir no solo el nombre de equipo o el nombre de host, sino también un nombre que pudiera identificar de forma inequívoca o completo ese equipo dentro de toda la jerarquía DNS. Ese nombre es el [*nombre de dominio completo*](f-gly.md) (FQDN), por ejemplo, server1.widgets.microsoft.com.

Sin embargo, en determinadas situaciones, la parte de la jerarquía de dominio del FQDN es complicada y se necesita un nombre local para un equipo determinado (o cualquier otro host DNS) relativo al dominio DNS en el que reside el host. Ese nombre es el [*nombre distintivo relativo*](r-gly.md). El nombre distintivo relativo es simplemente el nombre de host único a la izquierda del punto situado más a la izquierda en el FQDN, de modo que un FQDN de server1.widgets.microsoft.com tiene server1 como nombre distintivo relativo.

## <a name="relative-distinguished-name"></a>Nombre distintivo relativo

En lugar de imponer nuevos nombres o nuevas convenciones de nomenclatura a los usuarios de nombres NetBIOS, DNS simplemente usa el nombre de equipo (nombre de host) como nombre distintivo relativo y anexa la jerarquía de dominio DNS a ese nombre para crear el FQDN. En la ilustración siguiente se muestra cómo identificar la parte nombre-equipo (o nombre de host o nombre distintivo relativo) del FQDN:

![Rdn y la jerarquía de dominio dns se combinan para crear un fqdn](images/fqdn.png)

 

 




