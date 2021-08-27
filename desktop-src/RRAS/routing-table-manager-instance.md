---
title: Instancia del Administrador de tablas de enrutamiento
description: Una instancia de es una tabla independiente que el administrador de tablas de enrutamiento usa para mantener la información de enrutamiento sobre un subconjunto de interfaces.
ms.assetid: a17233fc-2c40-4d00-8a6b-86f08fef5690
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3215baf7a3cf093ecf47e8cf9965a71e75dea17a0527949e68b2c5f929d336ab
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120073925"
---
# <a name="routing-table-manager-instance"></a>Instancia del Administrador de tablas de enrutamiento

Una instancia de es una tabla independiente que el administrador de tablas de enrutamiento usa para mantener la información de enrutamiento sobre un subconjunto de interfaces. Las instancias se usan normalmente para permitir que un enrutador físico actúe como un conjunto de enrutadores virtuales: un enrutador virtual por red lógica.

Actualmente, el administrador de tablas de enrutamiento solo admite una instancia (identificada como cero, el valor predeterminado). El cliente puede registrarse con otras instancias, pero el administrador de enrutadores no reconoce ni usa ningún enrutador virtual, excepto el predeterminado.

 

 




