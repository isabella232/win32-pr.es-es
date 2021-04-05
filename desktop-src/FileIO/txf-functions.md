---
description: Funciones NTFS (TxF) transaccionales.
ms.assetid: fb6be33c-9d6c-48b2-a4da-31c60af8d972
title: Funciones TxF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b59fa3c9a1323ce77c97ee36390190ea6301d71d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103816798"
---
# <a name="txf-functions"></a>Funciones TxF

NTFS transaccional (TxF) proporciona las siguientes funciones.

## <a name="in-this-section"></a>En esta sección



| Función                                                                      | Descripción                                                                                                                  |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [**TxfLogCreateFileReadContext**](/windows/desktop/api/TxfW32/nf-txfw32-txflogcreatefilereadcontext)<br/> | Crea un contexto que se va a utilizar para leer los registros de replicación.<br/>                                                         |
| [**TxfLogDestroyReadContext**](/windows/desktop/api/TxfW32/nf-txfw32-txflogdestroyreadcontext)<br/>       | Cierra un contexto de lectura creado por la función [**TxfLogCreateFileReadContext**](/windows/desktop/api/TxfW32/nf-txfw32-txflogcreatefilereadcontext) .<br/> |
| [**TxfLogReadRecords**](/windows/desktop/api/TxfW32/nf-txfw32-txflogreadrecords)<br/>                     | Lee los registros de rehacer del registro.<br/>                                                                              |



 

 

 




