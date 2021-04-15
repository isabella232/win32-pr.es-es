---
title: Constantes DROPEFFECT (OleIdl. h)
description: Representa información sobre los efectos de una operación de arrastrar y colocar.
ms.assetid: d8e46899-3fbf-4012-8dd3-67fa627526d5
topic_type:
- apiref
api_name:
- DROPEFFECT_NONE
- DROPEFFECT_COPY
- DROPEFFECT_MOVE
- DROPEFFECT_LINK
- DROPEFFECT_SCROLL
api_location:
- OleIdl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2b1888aa028d4e047a9a8ec1f54e2497fa28ce4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105696048"
---
# <a name="dropeffect-constants"></a>Constantes de DROPEFFECT

Representa información sobre los efectos de una operación de arrastrar y colocar. La función [**DoDragDrop**](/windows/desktop/api/Ole2/nf-ole2-dodragdrop) y muchos de los métodos de [**IDropSource**](/windows/desktop/api/OleIdl/nn-oleidl-idropsource) y [**IDropTarget**](/windows/desktop/api/OleIdl/nn-oleidl-idroptarget) usan los valores de esta enumeración.



| Constante o valor                                                                                                                                                                                                                            | Descripción                                                                                                                         |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DROPEFFECT_NONE"></span><span id="dropeffect_none"></span><dl> <dt>**DROPEFFECT \_ NINGUNO**</dt> <dt>0</dt> </dl>                | El destino de colocación no puede aceptar los datos.<br/>                                                                                      |
| <span id="DROPEFFECT_COPY"></span><span id="dropeffect_copy"></span><dl> <dt>**DROPEFFECT \_ COPIAR**</dt> <dt>1</dt> </dl>                | Drop da como resultado una copia. El origen de arrastre no toca los datos originales.<br/>                                               |
| <span id="DROPEFFECT_MOVE"></span><span id="dropeffect_move"></span><dl> <dt>**DROPEFFECT \_ MOVIMIENTO**</dt> <dt>2</dt> </dl>                | El origen de arrastre debe quitar los datos. <br/>                                                                                     |
| <span id="DROPEFFECT_LINK"></span><span id="dropeffect_link"></span><dl> <dt>**DROPEFFECT \_ VÍNCULO**</dt> <dt>4</dt> </dl>                | Arrastrar origen debe crear un vínculo a los datos originales.<br/>                                                                   |
| <span id="DROPEFFECT_SCROLL"></span><span id="dropeffect_scroll"></span><dl> <dt>**DROPEFFECT \_ DESPLAZAMIENTO**</dt> <dt>0x80000000</dt> </dl> | El desplazamiento está a punto de iniciarse o está ocurriendo actualmente en el destino. Este valor se usa además de los demás valores.<br/> |



## <a name="remarks"></a>Observaciones

La aplicación siempre debe enmascarar los valores de la enumeración **DROPEFFECT** para garantizar la compatibilidad con implementaciones futuras. Actualmente, solo algunas de las posiciones de un valor de **DROPEFFECT** tienen significado. En el futuro, se agregarán más interpretaciones para los bits. Los orígenes de arrastre y los destinos de colocación deben enmascarar cuidadosamente estos valores adecuadamente antes de la comparación. Nunca deben comparar un **DROPEFFECT** con, por ejemplo, la copia DROPEFFECT, para lo que debe \_ hacer lo siguiente:

``` syntax
if (dwDropEffect == DROPEFFECT_COPY)... 
```

En su lugar, la aplicación siempre debe enmascarar el valor o los valores que se buscan como si utilizara una de las técnicas siguientes:

``` syntax
if (dwDropEffect & DROPEFFECT_COPY) == DROPEFFECT_COPY)...

if (dwDropEffect & DROPEFFECT_COPY)... 
```

Esto permite la definición de nuevos efectos de colocación, a la vez que conserva la compatibilidad con versiones anteriores con el código existente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>OleIdl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**DoDragDrop**](/windows/desktop/api/Ole2/nf-ole2-dodragdrop)
</dt> <dt>

[**IDropSource**](/windows/desktop/api/OleIdl/nn-oleidl-idropsource)
</dt> <dt>

[**IDropTarget**](/windows/desktop/api/OleIdl/nn-oleidl-idroptarget)
</dt> </dl>

 

 





