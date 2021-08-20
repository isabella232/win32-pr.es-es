---
title: Método IRDVTaskPlugin StartTask
description: Se llama para iniciar la tarea de actualización en la máquina virtual.
ms.assetid: c1e9f18b-1e83-4a29-8646-8adde94e8c14
ms.tgt_platform: multiple
keywords:
- Método StartTask Servicios de Escritorio remoto
- Método StartTask Servicios de Escritorio remoto , interfaz IRDVTaskPlugin
- Interfaz IRDVTaskPlugin Servicios de Escritorio remoto , método StartTask
topic_type:
- apiref
api_name:
- IRDVTaskPlugin.StartTask
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0e0bb9104ee1bbd3f0f6c2e8cc04b691205f2e40cb2221b79b5e9f251492a3a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118129262"
---
# <a name="irdvtaskpluginstarttask-method"></a>IrDVTaskPlugin::StartTask (método)

Se llama para iniciar la tarea de actualización en la máquina virtual.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT StartTask(
  [in] BSTR            Label,
  [in] BSTR            Identifier,
  [in] SAFEARRAY(BYTE) *Context
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Etiqueta* \[ En\]
</dt> <dd>

Etiqueta de la tarea. Esta es la etiqueta que se pasó al agente de desencadenador en el [**método ScheduleTask.**](irdvtaskpluginnotifysink-scheduletask.md)

</dd> <dt>

*Identificador* \[ En\]
</dt> <dd>

Identificador único de la tarea. Este es el identificador que se pasó al agente de desencadenador en el [**método ScheduleTask.**](irdvtaskpluginnotifysink-scheduletask.md)

</dd> <dt>

*Contexto* \[ En\]
</dt> <dd>

Datos opcionales para la tarea. Estos son los datos que se pasaron al agente de desencadenador en el [**método ScheduleTask.**](irdvtaskpluginnotifysink-scheduletask.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 Enterprise<br/>   |
| Servidor mínimo compatible<br/> | Windows Server 2008 R2<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IRDVTaskPlugin**](irdvtaskplugin.md)
</dt> </dl>

 

 





