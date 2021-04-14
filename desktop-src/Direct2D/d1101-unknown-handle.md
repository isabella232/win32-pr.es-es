---
title: D1101 identificador desconocido
ms.assetid: ae40058a-ea17-4262-87dc-0ce852c16c2a
description: Se le ha pasado una interfaz no asignada por este archivo DLL.
keywords:
- D1101 identificador desconocido de Direct2D
topic_type:
- apiref
api_name:
- D1101 Unknown Handle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 2a87491a02d3dea992f8dd767ad34cf83b2cbf40
ms.sourcegitcommit: 80ee822f6ebcbcc8f60042e0d14a39ef6989c731
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/27/2021
ms.locfileid: "105661452"
---
# <a name="d1101-unknown-handle"></a>D1101: identificador desconocido

\[  \] Se le ha pasado una interfaz de interfaz no asignada por este archivo dll.

## <a name="placeholders"></a>Marcadores de posición

<dl> <dt>

<span id="interface"></span><span id="INTERFACE"></span>*interfaz*
</dt> <dd>

Dirección de la interfaz.

</dd> </dl> 




 

## <a name="possible-causes"></a>Causas posibles

Uso de recursos no válido. El recurso creado fuera de Direct2D se usa con un generador de Direct2D o los recursos creados en un generador se usaban con un recurso creado por otro generador.

 

 




