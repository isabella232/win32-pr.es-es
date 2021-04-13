---
title: Método IRDVTaskPluginNotifySink (Sbtsv. h)
description: El agente de tareas lo llama para solicitar que se cierre el agente de tareas.
ms.assetid: 163e0ce5-f4ee-4242-bdbb-977c5ede3451
ms.tgt_platform: multiple
keywords:
- Método de terminación Servicios de Escritorio remoto
- Método de finalización Servicios de Escritorio remoto, interfaz IRDVTaskPluginNotifySink
- Interfaz IRDVTaskPluginNotifySink Servicios de Escritorio remoto, método he terminado
topic_type:
- apiref
api_name:
- IRDVTaskPluginNotifySink.OnTerminated
api_location:
- sbtsv.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b261437425b0b4dce4b2c2e17c52b6e24ea3e0e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535320"
---
# <a name="irdvtaskpluginnotifysinkonterminated-method"></a>IRDVTaskPluginNotifySink:: alterminad (método)

El agente de tareas lo llama para solicitar que se cierre el agente de tareas.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT OnTerminated(
  [in] HRESULT hr
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*HR* \[ de\]
</dt> <dd>

Indica si el apagado se debe a un apagado normal o a un error. Si el apagado es normal, contiene **S \_ correctos**. De lo contrario, contiene un código de error **HRESULT** .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 Enterprise<br/>                                                    |
| Servidor mínimo compatible<br/> | Windows Server 2008 R2<br/>                                                  |
| Encabezado<br/>                   | <dl> <dt>Sbtsv. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IRDVTaskPluginNotifySink**](irdvtaskpluginnotifysink.md)
</dt> </dl>

 

 





