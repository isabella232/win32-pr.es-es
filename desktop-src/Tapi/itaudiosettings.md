---
description: La interfaz ITAudioSettings expone métodos que permiten a una aplicación obtener y establecer parámetros para el control de un dispositivo de audio.
ms.assetid: 56607024-255d-4d1b-9ca0-6086eff7b7b2
title: Interfaz ITAudioSettings (Ipmsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85ce0c7a92e34583947be983ed4d28391eb70c02697313aedee21a7158c9c3b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119140388"
---
# <a name="itaudiosettings-interface"></a>Interfaz ITAudioSettings

\[Esta interfaz no está disponible para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente RTC proporciona una funcionalidad similar.\]

La **interfaz ITAudioSettings** expone métodos que permiten a una aplicación obtener y establecer parámetros para el control de un dispositivo de audio.

Esta interfaz se implementa mediante el [MSP de IPConf](ipconf-msp.md) y [el MSP H323](h323-msp.md). Solo se expone cuando una llamada usa estos proveedores de servicios.

## <a name="members"></a>Miembros

La **interfaz ITAudioSettings** hereda de [**la interfaz IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **ITAudioSettings también** tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz ITAudioSettings** tiene estos métodos.



| Método                                              | Descripción                                                                                                |
|:----------------------------------------------------|:-----------------------------------------------------------------------------------------------------------|
| [**Obtener**](/windows/desktop/api/tapi3if/nf-tapi3if-itasrterminalevent-get_call)          | Obtiene el valor de una propiedad de [configuración de audio determinada.](audiosettingsproperty.md)<br/>                  |
| [**GetRange**](/windows/desktop/api/tapi3if/nf-tapi3if-itasrterminalevent-get_terminal) | Obtiene el intervalo de valores válidos para una propiedad de [configuración de audio determinada.](audiosettingsproperty.md)<br/> |
| [**Establecer**](/windows/desktop/api/tapi3if/nf-tapi3if-itasrterminalevent-get_error)         | Establece el valor de una propiedad de [configuración de audio determinada.](audiosettingsproperty.md)<br/>                  |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|--------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3.1<br/>                                                         |
| Header<br/>       | <dl> <dt>Ipmsp.h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>Uuid.lib</dt> </dl>  |
| Archivo DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl> |



 

