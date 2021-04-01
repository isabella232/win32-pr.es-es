---
title: SystemMonitor. ScaleToFit, método
description: Ajustar los valores del contador para que quepan en el gráfico.
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
ms.openlocfilehash: b9a1e481dd44c441ea9e2dd44f2e63a06539da74
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801982"
---
# <a name="systemmonitorscaletofit-method"></a>SystemMonitor. ScaleToFit, método

Ajustar los valores del contador para que quepan en el gráfico.

## <a name="syntax"></a>Sintaxis


```VB
SystemMonitor.ScaleToFit( _
  ByVal selectedCountersOnly As Boolean _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*selectedCountersOnly* \[ de\]
</dt> <dd>

True para escalar solo los contadores seleccionados; de lo contrario, false para escalar todos los contadores.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Este método borrará la vista del gráfico. SYSMON usa el factor de escala especificado para cada contador para volver a dibujar el gráfico si el origen de datos es un archivo de registro o empezar a representar gráficamente nuevos valores de contador si el origen de datos es una actividad en tiempo real.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                  |
| Archivo DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SystemMonitor**](systemmonitor.md)
</dt> <dt>

[**Elemento de ScaleFactor**](counteritem-scalefactor.md)
</dt> <dt>

[**Contraelemento. seleccionado**](counteritem-selected.md)
</dt> </dl>

 

 





