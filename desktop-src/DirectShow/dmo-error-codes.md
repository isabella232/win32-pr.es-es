---
description: La tabla siguiente contiene códigos de error específicos de Microsoft DirectX media Objects (DMOs). Estos códigos de error se definen en el archivo de encabezado Mediaerr. h.
ms.assetid: 1ded5656-084d-4315-a414-aebf4a1820dc
title: Códigos de error de DMO (Mediaerr. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d76c8cd5e7001751cd2cf9eb7da4d88b2dc100bf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653943"
---
# <a name="dmo-error-codes"></a>Códigos de error de DMO

La tabla siguiente contiene códigos de error específicos de Microsoft DirectX media Objects (DMOs). Estos códigos de error se definen en el archivo de encabezado Mediaerr. h.



| Constante o valor                                                                                                                                                                                                                                                  | Descripción                                                                                                                                                         |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DMO_E_INVALIDSTREAMINDEX"></span><span id="dmo_e_invalidstreamindex"></span><dl> <dt>**DMO \_ E \_ INVALIDSTREAMINDEX**</dt> <dt>0x80040201</dt> </dl> | Índice de secuencia no válido.<br/>                                                                                                                                    |
| <span id="DMO_E_INVALIDTYPE"></span><span id="dmo_e_invalidtype"></span><dl> <dt>**DMO \_ E \_ INVALIDTYPE**</dt> <dt>0x80040202</dt> </dl>                      | Tipo de medio no válido.<br/>                                                                                                                                      |
| <span id="DMO_E_TYPE_NOT_SET"></span><span id="dmo_e_type_not_set"></span><dl> <dt>**DMO \_ E \_ tipo \_ no \_ establecido**</dt> <dt>0x80040203</dt> </dl>                 | No se estableció el tipo de medio. Una o más secuencias requieren un tipo de medio para poder realizar esta operación.<br/>                                                 |
| <span id="DMO_E_NOTACCEPTING"></span><span id="dmo_e_notaccepting"></span><dl> <dt>**DMO \_ E \_ NOTACCEPTING**</dt> <dt>0x80040204</dt> </dl>                   | No se pueden aceptar datos en esta secuencia. Es posible que tenga que procesar más datos de salida; vea [**IMediaObject::P rocessinput**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-processinput).<br/> |
| <span id="DMO_E_TYPE_NOT_ACCEPTED"></span><span id="dmo_e_type_not_accepted"></span><dl> <dt>**DMO \_ E \_ tipo \_ no \_ aceptado**</dt> <dt>0x80040205</dt> </dl>  | No se aceptó el tipo de medio.<br/>                                                                                                                             |
| <span id="DMO_E_NO_MORE_ITEMS"></span><span id="dmo_e_no_more_items"></span><dl> <dt>**DMO \_ E \_ no hay \_ más \_ elementos**</dt> <dt>0x80040206</dt> </dl>              | El índice de tipo de medio está fuera del intervalo.<br/>                                                                                                                        |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Mediaerr. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Constantes de DMO](dmo-constants.md)
</dt> </dl>

 

 




