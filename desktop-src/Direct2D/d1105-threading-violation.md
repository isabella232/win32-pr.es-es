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
ms.openlocfilehash: fe83baa32be8ae18948ae5a80e3e0b218cd4fa4a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127164137"
---
# <a name="d1105-threading-violation"></a>D1105: Infracción de subprocesos

Se ha accedido simultáneamente a una interfaz de subprocesos de alquiler \[  \] desde varios subprocesos.

## <a name="placeholders"></a>Marcadores de posición

<dl> <dt>

<span id="interface"></span><span id="INTERFACE"></span>*Interfaz*
</dt> <dd>

Dirección de la interfaz a la que han accedido varios subprocesos.

</dd> </dl> 




 

## <a name="possible-causes"></a>Causas posibles

Usar una instancia de objeto del mismo generador de subprocesos únicos de dos subprocesos diferentes.

 

 




