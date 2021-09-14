---
title: Método IMsTscAxEvents OnAuthenticationWarningDisplayed
description: Se llama antes de ActiveX control muestra un cuadro de diálogo de autenticación (por ejemplo, el cuadro de diálogo de error de certificado).
ms.assetid: ce307e5f-5e26-4041-bbd5-6871c0678da4
ms.tgt_platform: multiple
keywords:
- Método OnAuthenticationWarningDisplayed Servicios de Escritorio remoto
- Método OnAuthenticationWarningDisplayed Servicios de Escritorio remoto , interfaz IMsTscAxEvents
- Interfaz IMsTscAxEvents Servicios de Escritorio remoto método , OnAuthenticationWarningDisplayed
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnAuthenticationWarningDisplayed
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33307adf103536cce5841effe2843a7c48fda357
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126968212"
---
# <a name="imstscaxeventsonauthenticationwarningdisplayed-method"></a>IMsTscAxEvents::OnAuthenticationWarningDisplayed (método)

Se llama antes de ActiveX control muestra un cuadro de diálogo de autenticación (por ejemplo, el cuadro de diálogo de error de certificado).

## <a name="syntax"></a>Sintaxis


```C++
void OnAuthenticationWarningDisplayed();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Si es necesario, se puede usar la propiedad [**UIParentWindowHandle**](imsrdpclientnonscriptable2-uiparentwindowhandle.md) de la interfaz [**IMsRdpClientNonScriptable2**](imsrdpclientnonscriptable2.md) para asegurarse de que el cuadro de diálogo de autenticación modal que se va a mostrar esté primario en una ventana especificada (esto puede ser necesario para evitar que los usuarios usen otros cuadros de diálogo mientras se muestra el cuadro de diálogo de autenticación). De forma predeterminada, el elemento primario es ActiveX ventana de control.

Para obtener más información sobre Conexión web a Escritorio remoto, vea [Requisitos para Conexión web a Escritorio remoto](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                               |
| Servidor mínimo compatible<br/> | Windows Server 2008, Windows Server 2008 con SP1<br/>                           |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IMsTscAxEvents se define como 336d5562-efa8-482e-8cb3-c5c0fc7a7db6<br/>           |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**OnAuthenticationWarningDismissed**](imstscaxevents-onauthenticationwarningdismissed.md)
</dt> <dt>

[**UIParentWindowHandle**](imsrdpclientnonscriptable2-uiparentwindowhandle.md)
</dt> <dt>

[**IMsTscAxEvents**](imstscaxevents-interface.md)
</dt> </dl>

 

 





