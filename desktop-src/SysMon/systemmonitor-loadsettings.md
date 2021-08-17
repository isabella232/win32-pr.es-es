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
ms.openlocfilehash: 387bf2e42475d27f5440afb3fa0b945c910b3ac3bad610495936cd3a4a900bbc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118882330"
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

## <a name="remarks"></a>Comentarios

Para guardar los contadores actuales en el Monitor de sistema en un archivo HTML, llame al [**método SystemMonitor.SaveAs.**](systemmonitor-saveas.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                  |
| Archivo DLL<br/>                      | <dl> <dt>Sysmon.ocx</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Systemmonitor**](systemmonitor.md)
</dt> </dl>

 

 





