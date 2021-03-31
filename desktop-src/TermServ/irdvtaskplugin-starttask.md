---
title: IRDVTaskPlugin StartTask, método
description: Se llama para iniciar la tarea de actualización en la máquina virtual.
ms.assetid: c1e9f18b-1e83-4a29-8646-8adde94e8c14
ms.tgt_platform: multiple
keywords:
- Método StartTask Servicios de Escritorio remoto
- Método StartTask Servicios de Escritorio remoto, interfaz IRDVTaskPlugin
- Interfaz IRDVTaskPlugin Servicios de Escritorio remoto, método StartTask
topic_type:
- apiref
api_name:
- IRDVTaskPlugin.StartTask
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 51c499549378700a90d8fc78d075bc07c1f874cf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491320"
---
# <a name="irdvtaskpluginstarttask-method"></a>IRDVTaskPlugin:: StartTask (método)

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

*Etiqueta* \[ de de\]
</dt> <dd>

Etiqueta de la tarea. Esta es la etiqueta que se pasó al agente de desencadenador en el método [**ScheduleTask**](irdvtaskpluginnotifysink-scheduletask.md) .

</dd> <dt>

*Identificador de* \[ de\]
</dt> <dd>

Identificador único de la tarea. Este es el identificador que se pasó al agente de desencadenador en el método [**ScheduleTask**](irdvtaskpluginnotifysink-scheduletask.md) .

</dd> <dt>

*Contexto* \[ de de\]
</dt> <dd>

Datos opcionales para la tarea. Estos son los datos que se pasaron al agente de desencadenador en el método [**ScheduleTask**](irdvtaskpluginnotifysink-scheduletask.md) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 Enterprise<br/>   |
| Servidor mínimo compatible<br/> | Windows Server 2008 R2<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IRDVTaskPlugin**](irdvtaskplugin.md)
</dt> </dl>

 

 





