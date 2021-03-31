---
title: Constantes de TS_IAS_ (Textstor. h)
description: Las constantes de IAS de TS \_ \_ se usan como marcas de bits para controlar la inserción de texto o de objetos incrustados en una selección o un punto de inserción.
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150331"
---
# <a name="ts_ias_-constants"></a>\_Constantes de IAS de TS \_ \*

Las \_ constantes de IAS \_ \* de TS se utilizan como marcas de bits para controlar la inserción de texto o de objetos incrustados en una selección o un punto de inserción.



| Constante o valor                                                                                                                                                                                                                       | Descripción                                                                                                                                   |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TS_IAS_NOQUERY"></span><span id="ts_ias_noquery"></span><dl> <dt>**TS \_ \_NOquery de IAS**</dt> <dt>(0x1)</dt> </dl>       | Se inserta texto y el puntero de intervalo se establece en **null** al salir. No se puede combinar con la \_ marca QUERYONLY de IAS de TS \_ .<br/>          |
| <span id="TS_IAS_QUERYONLY"></span><span id="ts_ias_queryonly"></span><dl> <dt>**TS \_ \_QUERYONLY IAS**</dt> <dt>(0X2)</dt> </dl> | No realice la inserción. El autor de la llamada solo requiere que se establezca el puntero de intervalo. No se puede combinar con la \_ marca NOquery de IAS de TS \_ .<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                              |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                    |
| Redistribuible<br/>          | TSF 1,0 en Windows 2000 Professional<br/>                                         |
| Encabezado<br/>                   | <dl> <dt>Textstor. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Textstor. idl</dt> </dl> |



 

 





