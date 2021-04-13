---
title: SystemMonitor. LoadSettings, método
description: Agrega los contadores del archivo de plantilla HTML al monitor de sistema.
ms.assetid: 3f88e590-df2b-4861-8ee6-a08f8742e6ad
keywords:
- Método LoadSettings SysMon
- Método LoadSettings SysMon, objeto SystemMonitor
- Objeto SystemMonitor SysMon, Método LoadSettings
topic_type:
- apiref
api_name:
- SystemMonitor.LoadSettings
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e412ebfe97035c4847391a7cc9166cf512897bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422338"
---
# <a name="systemmonitorloadsettings-method"></a>SystemMonitor. LoadSettings, método

Agrega los contadores del archivo de plantilla HTML al monitor de sistema.

## <a name="syntax"></a>Sintaxis


```VB
SystemMonitor.LoadSettings( _
  ByVal SettingsFileName As String _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*SettingsFileName* \[ de\]
</dt> <dd>

Cadena HTML que especifica los contadores que se van a agregar al monitor del sistema.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Para guardar los contadores actuales en el monitor de sistema en un archivo HTML, llame al método [**SystemMonitor. SaveAs**](systemmonitor-saveas.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                  |
| Archivo DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SystemMonitor**](systemmonitor.md)
</dt> </dl>

 

 





