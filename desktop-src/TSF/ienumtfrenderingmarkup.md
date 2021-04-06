---
title: Interfaz IEnumTfRenderingMarkup
description: La interfaz IEnumTfRenderingMarkup se implementa mediante el administrador de TSF y la usan las aplicaciones. Esta interfaz se puede recuperar mediante ITfContextRenderingMarkup GetRenderingMarkup y enumera la información de marcado de representación.
ms.assetid: 6062a6f5-f973-4cd5-94d3-05aa418e0198
keywords:
- IEnumTfRenderingMarkup interface Text Services Framework
- IEnumTfRenderingMarkup interface Text Services Framework, descrito
topic_type:
- apiref
api_name:
- IEnumTfRenderingMarkup
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3005c8fe37a26b11f5155b639f8c151cf59c2cf0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104078163"
---
# <a name="ienumtfrenderingmarkup-interface"></a>Interfaz IEnumTfRenderingMarkup

La interfaz **IEnumTfRenderingMarkup** se implementa mediante el administrador de TSF y la usan las aplicaciones. Esta interfaz se puede recuperar mediante [ITfContextRenderingMarkup:: GetRenderingMarkup](itfcontextrenderingmarkup-getrenderingmarkup.md) y enumera la información de marcado de representación.



| Métodos IEnumTfRenderingMarkup            | Descripción                                                                                                                                            |
|-------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Clonar](ienumtfrenderingmarkup-clone.md) | El método **IEnumTfRenderingMarkup:: Clone** crea una copia del objeto de enumerador.                                                                  |
| [Siguiente](ienumtfrenderingmarkup-next.md)   | El método **IEnumTfRenderingMarkup:: Next** obtiene, desde la posición actual, el número especificado de elementos de la secuencia de enumeración.          |
| [Reset](ienumtfrenderingmarkup-reset.md) | El método **IEnumTfRenderingMarkup:: RESET** restablece el objeto de enumerador moviendo la posición actual al principio de la secuencia de enumeración. |
| [Skip](ienumtfrenderingmarkup-skip.md)   | El método **IEnumTfRenderingMarkup:: Skip** obtiene, desde la posición actual, el número especificado de elementos de la secuencia de enumeración.          |



 

## <a name="members"></a>Miembros

La interfaz **IEnumTfRenderingMarkup** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , pero no tiene miembros adicionales.

## <a name="remarks"></a>Observaciones

> [!Note]  
> Esta interfaz no está actualmente en los archivos de encabezado públicos. Para usar esta API, debe compilar MIDL en el [prototipo](prototypes.md).

 

 

 