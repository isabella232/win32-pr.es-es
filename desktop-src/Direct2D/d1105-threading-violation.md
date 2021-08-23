---
title: Infracción de subprocesos D1105
ms.assetid: 2c6cf90b-ce9e-4ea9-849d-22170f65ffb0
description: Se ha accedido simultáneamente a una interfaz de subprocesos de alquiler desde varios subprocesos.
keywords:
- D1105 Threading Violation Direct2D
topic_type:
- apiref
api_name:
- D1105 Threading Violation
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 12e7321fd40437bc262439c6ddb319a0aa6dba145d05d3feebba2813c904bbce
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119537975"
---
# <a name="d1105-threading-violation"></a>D1105: Infracción de subprocesos

Se ha accedido simultáneamente a una interfaz de subproceso de alquiler \[  \] desde varios subprocesos.

## <a name="placeholders"></a>Marcadores de posición

<dl> <dt>

<span id="interface"></span><span id="INTERFACE"></span>*Interfaz*
</dt> <dd>

Dirección de la interfaz a la que han accedido varios subprocesos.

</dd> </dl> 




 

## <a name="possible-causes"></a>Causas posibles

Usar una instancia de objeto del mismo generador de un solo subproceso de dos subprocesos diferentes.

 

 




