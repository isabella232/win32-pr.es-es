---
description: Para recuperar los elementos de una ruta de acceso, llame a la función PdhParseCounterPath. La función analiza los elementos de una ruta de acceso de contador y los devuelve en una estructura \_ PDH COUNTER \_ PATH \_ ELEMENTS.
ms.assetid: 65c722f9-6f9d-4e3d-abf3-867cf260ef9f
title: Obtener elementos de la ruta de acceso del contador a partir de una ruta de acceso de contador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08b8579033ddf7a97aec36b88bd067f9a240506d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062889"
---
# <a name="obtaining-counter-path-elements-from-a-counter-path"></a>Obtener elementos de la ruta de acceso del contador a partir de una ruta de acceso de contador

Para recuperar los elementos de una ruta de acceso, llame a la [**función PdhParseCounterPath.**](/windows/desktop/api/Pdh/nf-pdh-pdhparsecounterpatha) La función analiza los elementos de una ruta de acceso de contador y los devuelve en una [**estructura \_ PDH COUNTER \_ PATH \_ ELEMENTS.**](/windows/desktop/api/Pdh/ns-pdh-pdh_counter_path_elements_a)

Si tiene un nombre de instancia complejo (uno que contiene una instancia primaria y un índice de instancia), puede llamar a la función [**PdhParseInstanceName**](/windows/desktop/api/Pdh/nf-pdh-pdhparseinstancenamea) para extraer el nombre de instancia, el índice de instancia y el nombre primario.

 

 



