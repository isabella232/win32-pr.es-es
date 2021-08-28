---
title: Terminología esencial de canalización
description: Al igual que otros tipos de parámetros para llamadas a procedimientos remotos, las canalizaciones pueden ser parámetros \ in\ o \ out\.
ms.assetid: 377fb65a-e819-4e96-a5b7-9850afd97b73
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 389885f440faa477ab22f2100685e2955cbf9fb7ddc4ffcb6440dc4b6f68e003
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118930074"
---
# <a name="essential-pipe-terminology"></a>Terminología esencial de canalización

Al igual que otros tipos de parámetros para llamadas a procedimientos remotos, las canalizaciones pueden ser parámetros de entrada \[ [](/windows/desktop/Midl/in) \] \[ [**o**](/windows/desktop/Midl/out-idl) \] salida. Puesto que el servidor controla la transferencia de datos a través de una canalización, se dice que las canalizaciones con el atributo \[ **in** \] extraigan datos al  servidor. De forma similar, las *canalizaciones de salida* insertan datos del servidor al cliente. Los procedimientos que hacen la transferencia de datos se denominan procedimiento *de* extracción y procedimiento *de inserción*, respectivamente.

El compilador MIDL genera los procedimientos de inserción y extracción para el servidor. Además, administra la asignación de búferes de datos en memoria. Sin embargo, el cliente debe proporcionar sus propios procedimientos de inserción y extracción. También debe proporcionar un procedimiento para asignar los búferes de memoria utilizados por la canalización. El código auxiliar de cliente llama automáticamente a estos en el momento adecuado. El procedimiento de asignación se suele denominar procedimiento de asignación o función de asignación.

 

 