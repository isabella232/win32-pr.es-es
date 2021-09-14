---
description: La tabla siguiente contiene códigos de error específicos de objetos multimedia (DDO) de Microsoft DirectX. Estos códigos de error se definen en el archivo de encabezado Mediaerr.h.
ms.assetid: 1ded5656-084d-4315-a414-aebf4a1820dc
title: DMO Códigos de error (Mediaerr.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d76c8cd5e7001751cd2cf9eb7da4d88b2dc100bf
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127362422"
---
# <a name="dmo-error-codes"></a>DMO Códigos de error

La tabla siguiente contiene códigos de error específicos de objetos multimedia (DDO) de Microsoft DirectX. Estos códigos de error se definen en el archivo de encabezado Mediaerr.h.



| Constante o valor                                                                                                                                                                                                                                                  | Descripción                                                                                                                                                         |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DMO_E_INVALIDSTREAMINDEX"></span><span id="dmo_e_invalidstreamindex"></span><dl> <dt>**DMO \_ E \_ INVALIDSTREAMINDEX**</dt> <dt>0x80040201</dt> </dl> | Índice de secuencia no válido.<br/>                                                                                                                                    |
| <span id="DMO_E_INVALIDTYPE"></span><span id="dmo_e_invalidtype"></span><dl> <dt>**DMO \_ E \_ INVALIDTYPE**</dt> <dt>0x80040202</dt> </dl>                      | Tipo de medio no válido.<br/>                                                                                                                                      |
| <span id="DMO_E_TYPE_NOT_SET"></span><span id="dmo_e_type_not_set"></span><dl> <dt>**DMO \_ E \_ TYPE \_ NOT \_ SET**</dt> <dt>0x80040203</dt> </dl>                 | No se estableció el tipo de medio. Una o varias secuencias requieren un tipo de medio para poder realizar esta operación.<br/>                                                 |
| <span id="DMO_E_NOTACCEPTING"></span><span id="dmo_e_notaccepting"></span><dl> <dt>**DMO \_ E \_ NOTACCEPTING**</dt> <dt>0x80040204</dt> </dl>                   | No se pueden aceptar datos en esta secuencia. Es posible que tenga que procesar más datos de salida; vea [**IMediaObject::P rocessInput**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-processinput).<br/> |
| <span id="DMO_E_TYPE_NOT_ACCEPTED"></span><span id="dmo_e_type_not_accepted"></span><dl> <dt>**DMO \_ E \_ TYPE \_ NOT \_ ACCEPTED**</dt> <dt>0x80040205</dt> </dl>  | No se aceptó el tipo de medio.<br/>                                                                                                                             |
| <span id="DMO_E_NO_MORE_ITEMS"></span><span id="dmo_e_no_more_items"></span><dl> <dt>**DMO \_ E \_ NO \_ MORE \_ ITEMS**</dt> <dt>0x80040206</dt> </dl>              | El índice de tipo multimedia está fuera del intervalo.<br/>                                                                                                                        |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Mediaerr.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[DMO Constantes](dmo-constants.md)
</dt> </dl>

 

 




