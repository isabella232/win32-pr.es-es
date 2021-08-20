---
title: Método IRDVTaskPlugin Terminate
description: Se llama cuando se cierra el agente de tareas.
ms.assetid: b693a318-1da7-4207-8046-a62b7ccca471
ms.tgt_platform: multiple
keywords:
- Método Terminate Servicios de Escritorio remoto
- Método Terminate Servicios de Escritorio remoto interfaz , IRDVTaskPlugin
- Interfaz IRDVTaskPlugin Servicios de Escritorio remoto método , Terminate
topic_type:
- apiref
api_name:
- IRDVTaskPlugin.Terminate
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0ccfcb1a59f0db6d29881d139d16bd08308a40df2c1233beab66b0b4814caa84
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118129272"
---
# <a name="irdvtaskpluginterminate-method"></a>IRDVTaskPlugin::Terminate (Método)

Se llama cuando se cierra el agente de tareas.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Terminate(
  [in] HRESULT hr
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hr* \[ En\]
</dt> <dd>

Indica si el apagado se debe a un apagado normal o a un error. Si el apagado es normal, contiene **S \_ OK**. De lo contrario, contiene un código de error **HRESULT.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 Enterprise<br/>   |
| Servidor mínimo compatible<br/> | Windows Server 2008 R2<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IRDVTaskPlugin**](irdvtaskplugin.md)
</dt> </dl>

 

 





