---
description: El método FreeEventData libera el espacio asignado para la estructura NMEVENTDATA.
ms.assetid: f86dcfd8-5a3b-4ce3-9d45-04545b030a89
title: 'IMonitorEventer:: FreeEventData (método) (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMonitorEventer.FreeEventData
api_type:
- COM
api_location:
- Netmon.h
ms.openlocfilehash: c71b7563e00bfceb220ce1c2bf109339267fbabf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677273"
---
# <a name="imonitoreventerfreeeventdata-method"></a>IMonitorEventer:: FreeEventData (método)

El método **FreeEventData** libera el espacio asignado para la estructura [**NMEVENTDATA**](nmeventdata.md) .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT FreeEventData(
  [in] PNMEVENTDATA pNMEventData
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pNMEventData* \[ de\]
</dt> <dd>

Dirección de la estructura [**NMEVENTDATA**](nmeventdata.md) , cuya memoria se libera.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve S \_ correcto.

## <a name="remarks"></a>Observaciones

Los monitores llaman a este método para liberar la memoria que asignan a la estructura de datos del evento. Tenga en cuenta que mientras el monitor todavía tenga un puntero a cadenas en una estructura [**NMEVENTDATA**](nmeventdata.md) asignada, se debe liberar la memoria de estas cadenas antes de llamar al método **FreeEventData** .

Para obtener más información sobre cómo asignar memoria para una estructura [**NMEVENTDATA**](nmeventdata.md) , vea [**IMonitorEventer:: GetEventData**](imonitoreventer-geteventdata.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMonitorEventer**](imonitoreventer.md)
</dt> <dt>

[**IMonitorEventer::GetEventData**](imonitoreventer-geteventdata.md)
</dt> <dt>

[**NMEVENTDATA**](nmeventdata.md)
</dt> </dl>

 

 




