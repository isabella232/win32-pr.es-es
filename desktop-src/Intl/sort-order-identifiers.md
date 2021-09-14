---
description: En este tema se describen los identificadores de criterio de ordenación, que se pueden usar en la preparación de los identificadores de configuración regional.
ms.assetid: abef64b5-ca3f-4cb3-92f0-1b7286bfb686
title: Identificadores de criterio de ordenación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64a09d8f33285fc5665eff72bbfe1e2075597216
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127171930"
---
# <a name="sort-order-identifiers"></a>Identificadores de criterio de ordenación

En este tema se describen los identificadores de criterio de ordenación, que se pueden usar en la preparación de los [identificadores de configuración regional.](locale-identifiers.md) Un identificador de criterio de ordenación se define con el formato "sortorder", al final del nombre de configuración regional usado en el identificador, por \_ ejemplo, "de-DE phoneb", donde "phoneb" es el criterio de \_ ordenación. El identificador de configuración regional correspondiente se crea de la siguiente manera: `MAKELCID(MAKELANGID(LANG_GERMAN, SUBLANG_GERMAN), SORT_GERMAN_PHONE_BOOK)` .



| Constante                      | Nombre de la configuración regional                                                                                         | Significado                                                           |
|-------------------------------|-----------------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| ORDENAR \_ CHINO \_ BIG5           | zh-TW<br/> zh-HK<br/> zh-MO<br/>                                                  | Pedido big5 chino                                                |
| ORDENAR \_ \_ BOPOMOFO CHINO       | zh-TW \_ pronun                                                                                       | Pedido bopomofo chino tradicional                                |
| ORDENAR \_ LA LIBRETA DE \_ TELÉFONOS EN \_ CHINO    | zh-CN \_ phoneb<br/>                                                                            | Pedido de la libreta de teléfonos (apellidos) en chino                                |
| SORT \_ CHINESE \_ PRC            | Trazo zh-CN \_<br/> Trazo zh-HK \_<br/> Trazo de \_ zh-MO<br/> Trazo \_ zh-SG<br/> | Orden de recuento de trazos chino de PRC                                    |
| SORT \_ CHINESE \_ PRCP           | zh-CN<br/> zh-SG<br/>                                                                   | Orden fonético chino de PRC                                        |
| ORDENAR \_ \_ CHINO RADICALSTROKE  | zh-TW<br/> zh-HK<br/> zh-MO<br/>                                                  | Radical chino/orden de trazo                                      |
| ORDENAR \_ \_ UNICODE CHINO        | —                                                                                                   | Pedido Unicode **chino Windows 2000:** no se admite.<br/>  |
| SORT \_ DEFAULT                 | Nombre de configuración regional que es el mismo que el nombre de idioma correspondiente                                     | Orden de ordenación predeterminado                                                |
| SORTMODERN \_ \_ MODERN        | ka-GE \_ moderno                                                                                       | Orden moderno de ModernIdad                                             |
| ORDENAR \_ TRADICIONAL DE \_ SORT-TO-IN-SORT   | ka-GE                                                                                               | Orden tradicional de Trasnós                                        |
| ORDENACIÓN \_ DE LA LIBRETA TELEFÓNICA \_ \_ ALEMANA     | de-DE \_ phoneb                                                                                       | Pedido de la libreta de teléfonos en alemán                                           |
| ORDENAR \_ VALOR PREDETERMINADO DE \_ HÚNGARO      | hu-HU                                                                                               | Orden predeterminado húngaro                                           |
| ORDENACIÓN \_ TÉCNICA \_ DE HÚNGARO    | hu-HU \_ technl                                                                                       | Orden técnico húngaro                                         |
| SORT \_ JAPANESE \_ RADICALSTROKE | ja-JP                                                                                               | Orden de radical/trazo japonés                                     |
| ORDENAR \_ \_ UNICODE JAPONÉS       | —                                                                                                   | Pedido Unicode **japonés Windows 2000:** no se admite.<br/> |
| ORDENAR \_ \_ XJIS JAPONÉS          | ja-JP                                                                                               | Pedido XJIS japonés                                               |
| SORT \_ KOREAN \_ KSC             | ko-KR                                                                                               | Pedido de KSC coreano                                                  |
| ORDENAR \_ \_ UNICODE COREANO         | —                                                                                                   | Pedido Unicode **coreano Windows 2000:** no se admite.<br/>   |



 

 

 




