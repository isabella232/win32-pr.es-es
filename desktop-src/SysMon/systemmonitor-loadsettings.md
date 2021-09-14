---
title: Método SystemMonitor.LoadSettings
description: Agrega los contadores del archivo de plantilla HTML al Monitor de sistema.
ms.assetid: 3f88e590-df2b-4861-8ee6-a08f8742e6ad
keywords:
- Método LoadSettings SysMon
- Método LoadSettings SysMon , Objeto SystemMonitor
- Objeto SystemMonitor SysMon, método LoadSettings
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127374831"
---
# <a name="systemmonitorloadsettings-method"></a>Método SystemMonitor.LoadSettings

Agrega los contadores del archivo de plantilla HTML al Monitor de sistema.

## <a name="syntax"></a>Sintaxis


```VB
SystemMonitor.LoadSettings( _
  ByVal SettingsFileName As String _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*SettingsFileName* \[ En\]
</dt> <dd>

Cadena HTML que especifica los contadores que se agregarán al Monitor de sistema.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Para guardar los contadores actuales en el Monitor de sistema en un archivo HTML, llame al [**método SystemMonitor.SaveAs.**](systemmonitor-saveas.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                  |
| Archivo DLL<br/>                      | <dl> <dt>Sysmon.ocx</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Systemmonitor**](systemmonitor.md)
</dt> </dl>

 

 





