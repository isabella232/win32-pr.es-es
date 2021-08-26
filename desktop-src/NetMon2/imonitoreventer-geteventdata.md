---
description: El método GetEventData asigna espacio para las estructuras NMEVENTDATA y NMCOLUMNINFO.
ms.assetid: b24a2a30-4543-4311-87ec-66872463aed7
title: Método IMonitorEventer::GetEventData (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMonitorEventer.GetEventData
api_type:
- COM
api_location:
- Netmon.h
ms.openlocfilehash: 3a089e57ac5f66187f97dfa6ae7533aeda620632bdbf35c7b5bf3a34d4654b0c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120037375"
---
# <a name="imonitoreventergeteventdata-method"></a>IMonitorEventer::GetEventData (método)

El **método GetEventData** asigna espacio para las estructuras [NMEVENTDATA](nmeventdata.md) y [NMCOLUMNINFO.](nmcolumninfo.md)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetEventData(
  [in]  BYTE         bNumColumns,
  [out] PNMEVENTDATA *ppNMEventData
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*bNumColumns* \[ En\]
</dt> <dd>

Número de **estructuras NMCOLUMNINFO** necesarias.

</dd> <dt>

*ppNMEventData* \[ out\]
</dt> <dd>

Dirección de la **estructura NMEVENTDATA** que se devuelve.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método es correcto, el valor devuelto es S \_ OK.

Si el método no es correcto, el valor devuelto es NMERR \_ OUT \_ OF \_ MEMORY.

## <a name="remarks"></a>Comentarios

Los monitores llaman a este método para asignar memoria para las estructuras de información de columna y datos de eventos. Para liberar memoria asignada para una **estructura NMEVENTDATA,** vea [IMonitorEventer::FreeEventData](imonitoreventer-freeeventdata.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[IMonitorEventer](imonitoreventer.md)
</dt> <dt>

[IMonitorEventer::FreeEventData](imonitoreventer-freeeventdata.md)
</dt> <dt>

[NMEVENTDATA](nmeventdata.md)
</dt> <dt>

[NMCOLUMNINFO](nmcolumninfo.md)
</dt> </dl>

 

 




