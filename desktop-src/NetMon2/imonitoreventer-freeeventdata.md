---
description: El método FreeEventData libera espacio asignado para la estructura NMEVENTDATA.
ms.assetid: f86dcfd8-5a3b-4ce3-9d45-04545b030a89
title: Método IMonitorEventer::FreeEventData (Netmon.h)
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
ms.openlocfilehash: f2bf462ef63045c8c4e5822e3d28fc21b44dfeed5848da3ac89c8232dfacc062
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120037445"
---
# <a name="imonitoreventerfreeeventdata-method"></a>IMonitorEventer::FreeEventData (método)

El **método FreeEventData** libera espacio asignado para la [**estructura NMEVENTDATA.**](nmeventdata.md)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT FreeEventData(
  [in] PNMEVENTDATA pNMEventData
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pNMEventData* \[ En\]
</dt> <dd>

Dirección de la [**estructura NMEVENTDATA,**](nmeventdata.md) cuya memoria se libera.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve S \_ OK.

## <a name="remarks"></a>Comentarios

Los monitores llaman a este método para liberar la memoria que asignan para la estructura de datos de eventos. Tenga en cuenta que, aunque el monitor todavía tiene un puntero a cadenas en una estructura [**NMEVENTDATA**](nmeventdata.md) asignada, se debe liberar la memoria de estas cadenas antes de llamar al método **FreeEventData.**

Para obtener más información sobre cómo asignar memoria para una [**estructura NMEVENTDATA,**](nmeventdata.md) vea [**IMonitorEventer::GetEventData**](imonitoreventer-geteventdata.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMonitorEventer**](imonitoreventer.md)
</dt> <dt>

[**IMonitorEventer::GetEventData**](imonitoreventer-geteventdata.md)
</dt> <dt>

[**NMEVENTDATA**](nmeventdata.md)
</dt> </dl>

 

 




