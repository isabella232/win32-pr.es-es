---
description: La interfaz ITAudioSettings expone métodos que permiten a una aplicación obtener y establecer los parámetros para el control de un dispositivo de audio.
ms.assetid: 56607024-255d-4d1b-9ca0-6086eff7b7b2
title: Interfaz ITAudioSettings (Ipmsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eaf2566c7438dbcd14cdacee46cc4d5ec4166731
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690784"
---
# <a name="itaudiosettings-interface"></a>Interfaz ITAudioSettings

\[ Esta interfaz no está disponible para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente de RTC proporciona una funcionalidad similar.\]

La interfaz **ITAudioSettings** expone métodos que permiten a una aplicación obtener y establecer los parámetros para el control de un dispositivo de audio.

Esta interfaz la implementa [IPCONF MSP](ipconf-msp.md) y el MSP de [H323](h323-msp.md). Solo se expone cuando una llamada utiliza estos proveedores de servicios.

## <a name="members"></a>Miembros

La interfaz **ITAudioSettings** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **ITAudioSettings** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **ITAudioSettings** tiene estos métodos.



| Método                                              | Descripción                                                                                                |
|:----------------------------------------------------|:-----------------------------------------------------------------------------------------------------------|
| [**Obtener**](/windows/desktop/api/tapi3if/nf-tapi3if-itasrterminalevent-get_call)          | Obtiene el valor de una [propiedad de configuración de audio](audiosettingsproperty.md)determinada.<br/>                  |
| [**GetRange**](/windows/desktop/api/tapi3if/nf-tapi3if-itasrterminalevent-get_terminal) | Obtiene el intervalo de valores válidos para una [propiedad de configuración de audio](audiosettingsproperty.md)determinada.<br/> |
| [**Conjunto**](/windows/desktop/api/tapi3if/nf-tapi3if-itasrterminalevent-get_error)         | Establece el valor de una [propiedad de configuración de audio](audiosettingsproperty.md)determinada.<br/>                  |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|--------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3,1<br/>                                                         |
| Encabezado<br/>       | <dl> <dt>Ipmsp. h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>UUID. lib</dt> </dl>  |
| Archivo DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl> |



 

