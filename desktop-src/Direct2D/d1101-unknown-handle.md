---
title: D1101 Identificador desconocido
ms.assetid: ae40058a-ea17-4262-87dc-0ce852c16c2a
description: Se le pasó una interfaz no asignada por este archivo DLL.
keywords:
- D1101 Identificador desconocido Direct2D
topic_type:
- apiref
api_name:
- D1101 Unknown Handle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 37e84b9e5117732784267374ad9e6618e60d3b4020a6d23863b069b3b8233aa1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118161006"
---
# <a name="d1101-unknown-handle"></a>D1101: Identificador desconocido

Se le pasó una interfaz de interfaz no asignada \[  \] por este archivo DLL.

## <a name="placeholders"></a>Marcadores de posición

<dl> <dt>

<span id="interface"></span><span id="INTERFACE"></span>*Interfaz*
</dt> <dd>

Dirección de la interfaz.

</dd> </dl> 




 

## <a name="possible-causes"></a>Causas posibles

Uso de recursos no válido. El recurso creado fuera de Direct2D se usa con un generador de Direct2D o los recursos creados en una fábrica se usaron con un recurso creado por otra factoría.

 

 




