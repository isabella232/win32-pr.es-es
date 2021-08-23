---
title: Método OnWarning de IMsTscAxEvents
description: Se llama cuando el control de cliente encuentra una condición de error que no es grave.
ms.assetid: af43d3aa-0ae8-4721-b85d-bb043b20dc40
ms.tgt_platform: multiple
keywords:
- Método OnWarning Servicios de Escritorio remoto
- Método OnWarning Servicios de Escritorio remoto , interfaz IMsTscAxEvents
- Interfaz IMsTscAxEvents Servicios de Escritorio remoto , método OnWarning
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnWarning
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbcebe5c86bb50913ba11d4485f30757f399467aa30730f8cd27de50e360c0cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119657145"
---
# <a name="imstscaxeventsonwarning-method"></a>Método IMsTscAxEvents::OnWarning

Se llama cuando el control de cliente encuentra una condición de error que no es grave.

## <a name="syntax"></a>Sintaxis


```C++
void OnWarning(
  [in] long warningCode
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*warningCode* \[ En\]
</dt> <dd>

Código de error.

<dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

La caché de mapa de bits está dañada.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Para obtener más información sobre Conexión web a Escritorio remoto, vea [Requisitos para Conexión web a Escritorio remoto](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                               |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                         |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IMsTscAxEvents se define como 336d5562-efa8-482e-8cb3-c5c0fc7a7db6<br/>           |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMsTscAxEvents**](imstscaxevents-interface.md)
</dt> </dl>

 

 





