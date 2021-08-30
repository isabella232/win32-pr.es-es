---
description: La interfaz IKeyFrameControl se implementa mediante el MSP de H.323 y solo está disponible en objetos de secuencia H.323.
ms.assetid: 68cb1df1-f7fa-447a-8ea5-80dc1e802760
title: Interfaz IKeyFrameControl (H323priv.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4dac4890409fa67f3f5176502aa4bd156a7d78e8986b648e2824355acd78cdc6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119975866"
---
# <a name="ikeyframecontrol-interface"></a>Interfaz IKeyFrameControl

\[**IKeyFrameControl no** está disponible para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente RTC proporciona una funcionalidad similar.\]

La **interfaz IKeyFrameControl** se implementa mediante el [MSP de H.323](h323-msp.md) y solo está disponible en objetos de secuencia H.323. Esta interfaz expone métodos que permiten la creación y manipulación de terminales que pueden comunicarse entre clientes H323 y SDP. Tiene dos métodos que permiten a la aplicación solicitar al punto de conexión remoto que actualice la imagen de vídeo con un fotograma clave.

## <a name="members"></a>Miembros

La **interfaz IKeyFrameControl** hereda de la [**interfaz IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IKeyFrameControl también** tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IKeyFrameControl** tiene estos métodos.



| Método                                                                  | Descripción                                                                                 |
|:------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| [**PeriodicUpdatePicture**](ikeyframecontrol-periodicupdatepicture.md) | Configura un temporizador en la secuencia que pedirá actualizaciones de imágenes periódicamente.<br/> |
| [**UpdatePicture**](ikeyframecontrol-updatepicture.md)                 | Pide al remitente del vídeo que actualice la imagen.<br/>                                     |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|---------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3.0 o posterior<br/>                                                 |
| Header<br/>       | <dl> <dt>H323priv.h</dt> </dl> |
| Biblioteca<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| Archivo DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



## <a name="see-also"></a>Vea también

<dl> <dt>

[H323 MSP](h323-msp.md)
</dt> </dl>

 

