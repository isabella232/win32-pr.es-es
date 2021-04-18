---
description: En este tema se describen los identificadores de criterio de ordenación, que se pueden usar en la preparación de los identificadores de configuración regional.
ms.assetid: abef64b5-ca3f-4cb3-92f0-1b7286bfb686
title: Identificadores de criterio de ordenación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64a09d8f33285fc5665eff72bbfe1e2075597216
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361556"
---
# <a name="sort-order-identifiers"></a>Identificadores de criterio de ordenación

En este tema se describen los identificadores de criterio de ordenación, que se pueden usar en la preparación de los [identificadores de configuración regional](locale-identifiers.md). Un identificador de criterio de ordenación se define con el formato " \_ SortOrder", al final del nombre de la configuración regional que se usa en el identificador, por ejemplo, "de-de \_ Phoneb", donde "Phoneb" es el criterio de ordenación. El identificador de configuración regional correspondiente se crea como se indica a continuación: `MAKELCID(MAKELANGID(LANG_GERMAN, SUBLANG_GERMAN), SORT_GERMAN_PHONE_BOOK)` .



| Constante                      | Nombre de configuración regional                                                                                         | Significado                                                           |
|-------------------------------|-----------------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| ORDENAR \_ chino \_ Big5           | zh-TW<br/> zh-HK<br/> zh-MO<br/>                                                  | Orden chino BIG5                                                |
| ORDENAR \_ chino \_ BOPOMOFO       | zh-TW \_ pronun                                                                                       | Orden Bopomofo de chino tradicional                                |
| ORDENAR \_ la \_ Libreta de teléfonos de chino \_    | zh-CN \_ Phoneb<br/>                                                                            | Orden de las libretas de teléfonos de Chino (apellido)                                |
| ORDENAR \_ China China \_            | el trazo zh-CN \_<br/> trazo ZH-HK \_<br/> trazo ZH-MO \_<br/> gráfico ZH-SG \_<br/> | Orden de número de trazos de China China                                    |
| ORDENAR \_ chino \_ PRCP           | zh-CN<br/> zh-sg<br/>                                                                   | Orden fonético China China                                        |
| ORDENAR \_ chino \_ RADICALSTROKE  | zh-TW<br/> zh-HK<br/> zh-MO<br/>                                                  | El orden de los radicales y los trazos chinos                                      |
| ORDEN \_ \_ Unicode chino        | —                                                                                                   | **Windows 2000** de orden Unicode de chino: no se admite.<br/>  |
| ORDENAR \_ valores predeterminados                 | Nombre de configuración regional que coincide con el nombre de idioma correspondiente                                     | Orden de ordenación predeterminado                                                |
| ORDENAR \_ georgiano \_ moderno        | Ka-GE \_ moderno                                                                                       | Orden georgiano moderno                                             |
| ORDENAR \_ georgiano \_ tradicional   | ka-GE                                                                                               | Orden tradicional georgiano                                        |
| ORDENAR \_ el \_ listín de teléfonos alemanes \_     | de-DE \_ Phoneb                                                                                       | Orden de las libretas de teléfonos alemanas                                           |
| ORDENAR \_ de \_ forma predeterminada húngara      | hu-HU                                                                                               | Orden predeterminado Húngaro                                           |
| ORDENAR \_ Húngaro \_ técnico    | Hu-HU \_ technl                                                                                       | Orden técnico Húngaro                                         |
| ORDENAR \_ \_ RADICALSTROKE japonés | ja-JP                                                                                               | El orden de los trazos y los radicales japoneses                                     |
| ORDENAR \_ \_ Unicode en Japonés       | —                                                                                                   | **Windows 2000** de orden Unicode en Japonés: no se admiten.<br/> |
| ORDENAR \_ \_ XJIS japonés          | ja-JP                                                                                               | Orden XJIS japonés                                               |
| ORDENAR \_ Coreano \_ KSC             | ko-KR                                                                                               | Orden KSC Coreano                                                  |
| ORDENAR \_ \_ Unicode Coreano         | —                                                                                                   | **Windows 2000** de orden Unicode Coreano: no compatible.<br/>   |



 

 

 




