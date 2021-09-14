---
title: TS_IAS_ constantes (Textstor.h)
description: Las constantes IAS \ de TS se usan como marcas de campo de bits para controlar la inserción de texto u objetos \_ \_ incrustados en un punto de selección o inserción.
ms.assetid: 58e0d13c-d90c-41d2-bd93-4eba5fe0a69a
topic_type:
- apiref
api_name:
- TS_IAS_NOQUERY
- TS_IAS_QUERYONLY
api_location:
- Textstor.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d59584295567c586ebd8db7e5f63366fd8272f0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127068784"
---
# <a name="ts_ias_-constants"></a>Constantes \_ de IAS \_ \* de TS

Las constantes de TS IAS se usan como marcas de campo de bits para controlar la inserción de texto u objetos \_ \_ \* incrustados en un punto de selección o inserción.



| Constante o valor                                                                                                                                                                                                                       | Descripción                                                                                                                                   |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TS_IAS_NOQUERY"></span><span id="ts_ias_noquery"></span><dl> <dt>**TS \_ IAS \_ NOQUERY**</dt> <dt>( 0x1 )</dt> </dl>       | Se inserta texto y el puntero de intervalo se establece en **NULL al** salir. No se puede combinar con la marca \_ QUERYONLY de IAS de TS. \_<br/>          |
| <span id="TS_IAS_QUERYONLY"></span><span id="ts_ias_queryonly"></span><dl> <dt>**TS \_ IAS \_ QUERYONLY**</dt> <dt>( 0x2 )</dt> </dl> | No realice la inserción. El autor de la llamada solo requiere que se establezca el puntero de intervalo. No se puede combinar con la marca \_ NOQUERY de IAS de \_ TS.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                              |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                    |
| Redistribuible<br/>          | TSF 1.0 en Windows 2000 Professional<br/>                                         |
| Encabezado<br/>                   | <dl> <dt>Textstor.h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Textstor.idl</dt> </dl> |



 

 





