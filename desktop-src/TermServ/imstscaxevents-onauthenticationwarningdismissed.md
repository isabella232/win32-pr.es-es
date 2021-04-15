---
title: IMsTscAxEvents OnAuthenticationWarningDismissed, método
description: Se llama después de que un control ActiveX muestre un cuadro de diálogo de autenticación (por ejemplo, el cuadro de diálogo error de certificado).
ms.assetid: bf5dbe4a-9129-47b3-9808-ed09d9010099
ms.tgt_platform: multiple
keywords:
- Método OnAuthenticationWarningDismissed Servicios de Escritorio remoto
- Método OnAuthenticationWarningDismissed Servicios de Escritorio remoto, interfaz IMsTscAxEvents
- Interfaz IMsTscAxEvents Servicios de Escritorio remoto, método OnAuthenticationWarningDismissed
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnAuthenticationWarningDismissed
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86bdadfdbc8e0a1387a1f3aaf712188689d0f808
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422274"
---
# <a name="imstscaxeventsonauthenticationwarningdismissed-method"></a>IMsTscAxEvents:: OnAuthenticationWarningDismissed (método)

Se llama después de que un control ActiveX muestre un cuadro de diálogo de autenticación (por ejemplo, el cuadro de diálogo error de certificado).

## <a name="syntax"></a>Sintaxis


```C++
void OnAuthenticationWarningDismissed();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Si es necesario, se puede usar la propiedad [**UIParentWindowHandle**](imsrdpclientnonscriptable2-uiparentwindowhandle.md) de la interfaz [**IMsRdpClientNonScriptable2**](imsrdpclientnonscriptable2.md) para revertir cualquier elemento primario que pueda haberse realizado en el método [**OnAuthenticationWarningDisplayed**](imstscaxevents-onauthenticationwarningdisplayed.md) .

Para obtener más información acerca de Conexión web a Escritorio remoto, consulte [Requirements for conexión web a escritorio remoto](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                               |
| Servidor mínimo compatible<br/> | Windows Server 2008, Windows Server 2008 con SP1<br/>                           |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IMsTscAxEvents se define como 336d5562-efa8-482e-8cb3-c5c0fc7a7db6<br/>           |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**OnAuthenticationWarningDisplayed**](imstscaxevents-onauthenticationwarningdisplayed.md)
</dt> <dt>

[**UIParentWindowHandle**](imsrdpclientnonscriptable2-uiparentwindowhandle.md)
</dt> <dt>

[**IMsTscAxEvents**](imstscaxevents-interface.md)
</dt> </dl>

 

 





