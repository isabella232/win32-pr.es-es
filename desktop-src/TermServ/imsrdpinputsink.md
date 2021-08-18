---
title: Interfaz IMsRdpInputSink
description: Receptor de entrada de Escritorio remoto.
ms.assetid: ec30b64a-63bb-4f8f-8979-ab2ef9ece6b0
ms.tgt_platform: multiple
keywords:
- Interfaz IMsRdpInputSink Servicios de Escritorio remoto
- Interfaz IMsRdpInputSink Servicios de Escritorio remoto , descrito
topic_type:
- apiref
api_name:
- IMsRdpInputSink
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2167106577a005f6e4ba13ee77edcdbc77302efad9de00395fc7360ade4c5720
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119058852"
---
# <a name="imsrdpinputsink-interface"></a>Interfaz IMsRdpInputSink

Receptor de entrada de Escritorio remoto.

## <a name="members"></a>Miembros

La **interfaz IMsRdpInputSink** hereda de la [**interfaz IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IMsRdpInputSink** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IMsRdpInputSink** tiene estos métodos.



| Método                                                               | Descripción                          |
|:---------------------------------------------------------------------|:-------------------------------------|
| [**AddTouchInput**](/previous-versions/windows/desktop/legacy/mt786987(v=vs.85))               | Agrega entrada táctil.<br/>         |
| [**BeginTouchFrame**](/previous-versions/windows/desktop/legacy/mt786988(v=vs.85))           | Comience el marco táctil.<br/>        |
| [**EndTouchFrame**](/previous-versions/windows/desktop/legacy/mt786989(v=vs.85))               | Marco táctil final.<br/>          |
| [**SendKeyboardEvent**](/previous-versions/windows/desktop/legacy/mt786990(v=vs.85))       | Envía el evento de teclado.<br/>     |
| [**SendMouseButtonEvent**](/previous-versions/windows/desktop/legacy/mt786991(v=vs.85)) | Envía el evento del botón del mouse.<br/> |
| [**SendMouseMoveEvent**](/previous-versions/windows/desktop/legacy/mt786992(v=vs.85))     | Envía el evento de movimiento del mouse.<br/>   |
| [**SendMouseWheelEvent**](/previous-versions/windows/desktop/legacy/mt786993(v=vs.85))   | Envía el evento de rueda del mouse.<br/>  |
| [**SendSyncEvent**](/previous-versions/windows/desktop/legacy/mt786994(v=vs.85))               | Envía el evento de sincronización.<br/>         |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8.1<br/>                                                                 |
| Servidor mínimo compatible<br/> | Windows Server 2012 R2<br/>                                                      |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsRdpInputSink se define como 4606850E-76A7-4E28-A47E-C7174F619351<br/>     |



 

