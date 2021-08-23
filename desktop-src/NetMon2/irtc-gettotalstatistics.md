---
description: 'Método IRTC::GetTotalStatistics: el método GetTotalStatistics recupera las estadísticas totales de la captura actual.'
ms.assetid: e5098984-c69e-4cd5-9143-d85dfcbd7b92
title: Método IRTC::GetTotalStatistics (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC.GetTotalStatistics
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: c2b5187ab0afb432e845c74d29144c02edf94cdb62f291ae69e88ea5a5fdf198
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119063875"
---
# <a name="irtcgettotalstatistics-method"></a>IrTC::GetTotalStatistics (método)

El **método GetTotalStatistics** recupera las [*estadísticas totales*](t.md) de la captura [*actual.*](c.md)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT STDMETHODCALLTYPE GetTotalStatistics(
  [out] LPSTATISTICS lpStats,
  [in]  BOOL         fClearAfterReading
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lpStats* \[ out\]
</dt> <dd>

Puntero a una [estructura STATISTICS](statistics.md) que proporciona las estadísticas totales de la captura. Los autores de la llamada son responsables de asignar y liberar la memoria utilizada por la **estructura STATISTICS.**

</dd> <dt>

*fClearAfterReading* \[ En\]
</dt> <dd>

Marca que se usa para Monitor de red cómo controlar el almacenamiento interno de las estadísticas totales. Una configuración **de TRUE** indica Monitor de red borrar el almacenamiento interno de las estadísticas totales después de recuperar la información actual.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método es correcto, el valor devuelto es NMERR \_ SUCCESS.

Si el método no se realiza correctamente, el valor devuelto es uno de los siguientes códigos de error:



| Código devuelto                                                                                          | Descripción                                                                                                                   |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ NO \_ CONECTADO**</dt> </dl> | El NPP no está conectado a la red. Llame [a IRTC::Conectar](irtc-connect.md) para conectar el NPP a la red.<br/> |
| <dl> <dt>**NMERR \_ NOT \_ REALTIME**</dt> </dl>  | El NPP está conectado a la red, pero no con el [método IRTC::Conectar.](irtc-connect.md)<br/>                     |
| <dl> <dt>**NMERR \_ NO \_ CAPTURA**</dt> </dl> | El NPP no captura datos. Llame [a IRTC::Start](irtc-start.md) para empezar a capturar datos.<br/>                         |



 

## <a name="remarks"></a>Comentarios

Este método devuelve datos solo mientras una captura está en curso, incluso mientras la captura está en pausa.

Monitor de red también almacena las [*estadísticas de conversación*](c.md). Para recuperar las estadísticas de conversación, llame [al método IRTC::GetConversationStatistics.](irtc-getconversationstatistics.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                                                                     |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl>                                                                      |
| Archivo DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[IRTC](irtc.md)
</dt> <dt>

[IRTC::Conectar](irtc-connect.md)
</dt> <dt>

[IRTC::GetConversationStatistics](irtc-getconversationstatistics.md)
</dt> <dt>

[IRTC::Start](irtc-start.md)
</dt> <dt>

[Estadísticas](statistics.md)
</dt> </dl>

 

 




