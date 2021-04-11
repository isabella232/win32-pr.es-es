---
description: El método GetEventData asigna espacio para las estructuras NMEVENTDATA y NMCOLUMNINFO.
ms.assetid: b24a2a30-4543-4311-87ec-66872463aed7
title: 'IMonitorEventer:: GetEventData (método) (Netmon. h)'
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
ms.openlocfilehash: be1654c38f51fa62909e10c12900c087bf0842fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275338"
---
# <a name="imonitoreventergeteventdata-method"></a>IMonitorEventer:: GetEventData (método)

El método **GetEventData** asigna espacio para las estructuras [NMEVENTDATA](nmeventdata.md) y [NMCOLUMNINFO](nmcolumninfo.md) .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetEventData(
  [in]  BYTE         bNumColumns,
  [out] PNMEVENTDATA *ppNMEventData
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*bNumColumns* \[ de\]
</dt> <dd>

Número de estructuras **NMCOLUMNINFO** necesarias.

</dd> <dt>

*ppNMEventData* \[ enuncia\]
</dt> <dd>

Dirección de la estructura **NMEVENTDATA** que se devuelve.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método se realiza correctamente, el valor devuelto es S \_ OK.

Si el método no se realiza correctamente, el valor devuelto es \_ NMERR \_ de \_ memoria insuficiente.

## <a name="remarks"></a>Observaciones

Los monitores llaman a este método para asignar memoria para los datos de evento y las estructuras de información de columnas. Para liberar memoria asignada para una estructura **NMEVENTDATA** , vea [IMonitorEventer:: FreeEventData](imonitoreventer-freeeventdata.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



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

 

 




