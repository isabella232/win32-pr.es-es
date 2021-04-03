---
title: Instancia del administrador de tablas de enrutamiento
description: Una instancia es una tabla independiente que utiliza el administrador de tablas de enrutamiento para mantener la información de enrutamiento sobre un subconjunto de interfaces.
ms.assetid: a17233fc-2c40-4d00-8a6b-86f08fef5690
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d209f254bb9111c786bde6635b43895604785d5b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075624"
---
# <a name="routing-table-manager-instance"></a>Instancia del administrador de tablas de enrutamiento

Una instancia es una tabla independiente que utiliza el administrador de tablas de enrutamiento para mantener la información de enrutamiento sobre un subconjunto de interfaces. Las instancias se usan normalmente para permitir que un enrutador físico actúe como un conjunto de enrutadores virtuales, un enrutador virtual por red lógica.

Actualmente, el administrador de tabla de enrutamiento solo admite una instancia (identificada como cero, valor predeterminado). El cliente puede registrarse con otras instancias, pero el administrador de enrutador no reconoce ni usa ningún enrutador virtual, excepto el predeterminado.

 

 




