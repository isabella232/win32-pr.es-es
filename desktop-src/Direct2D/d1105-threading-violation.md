---
title: Infracción de subprocesamiento de D1105
ms.assetid: 2c6cf90b-ce9e-4ea9-849d-22170f65ffb0
description: Se tuvo acceso a una interfaz de subprocesos de alquiler simultáneamente desde varios subprocesos.
keywords:
- D1105 infracción de subprocesos Direct2D
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
ms.sourcegitcommit: 80ee822f6ebcbcc8f60042e0d14a39ef6989c731
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/27/2021
ms.locfileid: "105661450"
---
# <a name="d1105-threading-violation"></a>D1105: infracción de subprocesos

Se tuvo acceso simultáneamente a una interfaz de interfaz de subprocesos \[  \] de alquiler desde varios subprocesos.

## <a name="placeholders"></a>Marcadores de posición

<dl> <dt>

<span id="interface"></span><span id="INTERFACE"></span>*interfaz*
</dt> <dd>

Dirección de la interfaz a la que se ha tenido acceso a través de varios subprocesos.

</dd> </dl> 




 

## <a name="possible-causes"></a>Causas posibles

Usar una instancia de objeto del mismo generador de un solo subproceso de dos subprocesos diferentes.

 

 




