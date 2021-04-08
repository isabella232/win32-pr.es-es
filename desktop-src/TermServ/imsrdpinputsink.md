---
title: Interfaz IMsRdpInputSink
description: Receptor de entrada de escritorio remoto.
ms.assetid: ec30b64a-63bb-4f8f-8979-ab2ef9ece6b0
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la interfaz IMsRdpInputSink
- Servicios de Escritorio remoto de la interfaz IMsRdpInputSink, descrito
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
ms.openlocfilehash: cad3112b3bb6df92bfb7e403e779773a2203f2cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996140"
---
# <a name="imsrdpinputsink-interface"></a>Interfaz IMsRdpInputSink

Receptor de entrada de escritorio remoto.

## <a name="members"></a>Miembros

La interfaz **IMsRdpInputSink** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IMsRdpInputSink** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **IMsRdpInputSink** tiene estos métodos.



| Método                                                               | Descripción                          |
|:---------------------------------------------------------------------|:-------------------------------------|
| [**AddTouchInput**](/previous-versions/windows/desktop/legacy/mt786987(v=vs.85))               | Agrega una entrada táctil.<br/>         |
| [**BeginTouchFrame**](/previous-versions/windows/desktop/legacy/mt786988(v=vs.85))           | Iniciar el marco táctil.<br/>        |
| [**EndTouchFrame**](/previous-versions/windows/desktop/legacy/mt786989(v=vs.85))               | Fin del marco táctil.<br/>          |
| [**SendKeyboardEvent**](/previous-versions/windows/desktop/legacy/mt786990(v=vs.85))       | Envía el evento de teclado.<br/>     |
| [**SendMouseButtonEvent**](/previous-versions/windows/desktop/legacy/mt786991(v=vs.85)) | Envía el evento de botón del mouse.<br/> |
| [**SendMouseMoveEvent**](/previous-versions/windows/desktop/legacy/mt786992(v=vs.85))     | Envía el evento de movimiento del mouse.<br/>   |
| [**SendMouseWheelEvent**](/previous-versions/windows/desktop/legacy/mt786993(v=vs.85))   | Envía el evento de rueda del mouse.<br/>  |
| [**SendSyncEvent**](/previous-versions/windows/desktop/legacy/mt786994(v=vs.85))               | Envía el evento de sincronización.<br/>         |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8.1<br/>                                                                 |
| Servidor mínimo compatible<br/> | Windows Server 2012 R2<br/>                                                      |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsRdpInputSink se define como 4606850E-76A7-4E28-A47E-C7174F619351<br/>     |



 

