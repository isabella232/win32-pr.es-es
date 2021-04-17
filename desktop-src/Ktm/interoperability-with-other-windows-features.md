---
description: El Coordinador de transacciones distribuidas (DTC) permite transacciones distribuidas o transacciones que están bajo el control de varios administradores de recursos en uno o varios sistemas. KTM y DTC funcionan conjuntamente para lograrlo.
ms.assetid: 468379e2-c5f6-479f-9d5d-42afb395ec9b
title: Interoperabilidad con otras características de Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa3aeac3d920b408a9a18c32eab83cf747525e82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687831"
---
# <a name="interoperability-with-other-windows-features"></a>Interoperabilidad con otras características de Windows

El [Coordinador de transacciones distribuidas](/previous-versions/windows/desktop/ms684146(v=vs.85)) (DTC) permite *transacciones distribuidas* o transacciones que están bajo el control de varios administradores de recursos en uno o varios sistemas. KTM y DTC funcionan conjuntamente para lograrlo.

COM+ expone un modelo declarativo para la programación transaccional. En otras palabras, el programador declara la medida en la que un objeto puede aprovechar las transacciones y el tiempo de ejecución de COM+ administra las transacciones en nombre del objeto. Por ejemplo, un objeto se puede declarar para que participe en una transacción solo si ya existe una, para requerir una transacción (se crea una si aún no existe), para requerir una nueva transacción (se crea una con independencia de si ya existe) o no es transaccional. Estas transacciones administradas mediante declaración se utilizan automáticamente en las conexiones de base de datos creadas por objetos COM+ que se ejecutan en el contexto de una transacción.

 

 
