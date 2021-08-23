---
description: Para recuperar los elementos de una ruta de acceso, llame a la función PdhParseCounterPath. La función analiza los elementos de una ruta de acceso de contador y los devuelve en una estructura \_ PDH COUNTER \_ PATH \_ ELEMENTS.
ms.assetid: 65c722f9-6f9d-4e3d-abf3-867cf260ef9f
title: Obtener elementos de ruta de acceso de contador a partir de una ruta de acceso de contador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 479c8df5c7176684fc439f632a22f829afe5afae202f7595579350450ee30c8f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119143978"
---
# <a name="obtaining-counter-path-elements-from-a-counter-path"></a>Obtener elementos de ruta de acceso de contador a partir de una ruta de acceso de contador

Para recuperar los elementos de una ruta de acceso, llame a la [**función PdhParseCounterPath.**](/windows/desktop/api/Pdh/nf-pdh-pdhparsecounterpatha) La función analiza los elementos de una ruta de acceso de contador y los devuelve en una [**estructura \_ PDH COUNTER \_ PATH \_ ELEMENTS.**](/windows/desktop/api/Pdh/ns-pdh-pdh_counter_path_elements_a)

Si tiene un nombre de instancia complejo (uno que contiene una instancia primaria y un índice de instancia), puede llamar a la función [**PdhParseInstanceName**](/windows/desktop/api/Pdh/nf-pdh-pdhparseinstancenamea) para extraer el nombre de instancia, el índice de instancia y el nombre primario.

 

 



