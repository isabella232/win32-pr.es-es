---
title: Instancia de Routing Table Manager
description: Una instancia de es una tabla independiente que el administrador de tablas de enrutamiento usa para mantener la información de enrutamiento sobre un subconjunto de interfaces.
ms.assetid: a17233fc-2c40-4d00-8a6b-86f08fef5690
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d209f254bb9111c786bde6635b43895604785d5b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073849"
---
# <a name="routing-table-manager-instance"></a>Instancia de Routing Table Manager

Una instancia de es una tabla independiente que el administrador de tablas de enrutamiento usa para mantener la información de enrutamiento sobre un subconjunto de interfaces. Las instancias se usan normalmente para permitir que un enrutador físico actúe como un conjunto de enrutadores virtuales: un enrutador virtual por red lógica.

Actualmente, el administrador de tablas de enrutamiento solo admite una instancia (identificada como cero, el valor predeterminado). El cliente puede registrarse con otras instancias, pero el administrador de enrutadores no reconoce ni usa ningún enrutador virtual, excepto el predeterminado.

 

 




