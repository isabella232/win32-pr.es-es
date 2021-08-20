---
title: Método SystemMonitor.ScaleToFit
description: Escale los valores del contador para que quepa en el gráfico.
ms.assetid: 8e58e51a-4767-40da-836a-e49d34dec195
keywords:
- Método ScaleToFit SysMon
- Método ScaleToFit SysMon, objeto SystemMonitor
- Objeto SystemMonitor SysMon, método ScaleToFit
topic_type:
- apiref
api_name:
- SystemMonitor.ScaleToFit
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1cddb539f8c8d2c6c78f70d96d82da171e11a62afbeaa31d1a011c74c2cb096d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118881519"
---
# <a name="systemmonitorscaletofit-method"></a>Método SystemMonitor.ScaleToFit

Escale los valores del contador para que quepa en el gráfico.

## <a name="syntax"></a>Sintaxis


```VB
SystemMonitor.ScaleToFit( _
  ByVal selectedCountersOnly As Boolean _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*selectedCountersOnly* \[ En\]
</dt> <dd>

True para escalar solo los contadores seleccionados; de lo contrario, false para escalar todos los contadores.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Este método borrará la vista de gráfico. A continuación, SYSMON usa el factor de escala especificado para cada contador para volver a dibujar el gráfico si el origen de datos es un archivo de registro o comenzar a crear gráficos de nuevos valores de contador si el origen de datos es una actividad en tiempo real.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                  |
| Archivo DLL<br/>                      | <dl> <dt>Sysmon.ocx</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Systemmonitor**](systemmonitor.md)
</dt> <dt>

[**CounterItem.ScaleFactor**](counteritem-scalefactor.md)
</dt> <dt>

[**CounterItem.Selected**](counteritem-selected.md)
</dt> </dl>

 

 





