---
description: La interfaz ITAudioDeviceControl expone métodos que permiten a una aplicación obtener y establecer los parámetros para el control de un dispositivo de audio.
ms.assetid: 9a557cb2-acad-406c-9a87-18cbe96e8a9f
title: Interfaz ITAudioDeviceControl (Ipmsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 589bf50ee219f200a81aed7057b7755f203b2275
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680940"
---
# <a name="itaudiodevicecontrol-interface"></a>Interfaz ITAudioDeviceControl

\[ Esta interfaz no está disponible para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente de RTC proporciona una funcionalidad similar.\]

La interfaz **ITAudioDeviceControl** expone métodos que permiten a una aplicación obtener y establecer los parámetros para el control de un dispositivo de audio.

Esta interfaz la implementa [IPCONF MSP](ipconf-msp.md) y el MSP de [H323](h323-msp.md). Se expone cuando una llamada utiliza estos proveedores de servicios o un proveedor de servicios de terceros que implementa esta interfaz. Para obtener un puntero a la interfaz **ITAudioDeviceControl** , llame a **QueryInterface** en la interfaz [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream) que controla el dispositivo de audio correspondiente a la secuencia. El tipo de medio de la interfaz **ITStream** debe ser audio para que se exponga la interfaz **ITAudioDeviceControl** .

## <a name="members"></a>Miembros

La interfaz **ITAudioDeviceControl** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **ITAudioDeviceControl** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **ITAudioDeviceControl** tiene estos métodos.



| Método                                              | Descripción                                                                                             |
|:----------------------------------------------------|:--------------------------------------------------------------------------------------------------------|
| [**Obtener**](/windows/desktop/api/tapi3if/nf-tapi3if-itasrterminalevent-get_call)          | Obtiene el valor de una [propiedad de dispositivo de audio](audiodeviceproperty.md)determinada.<br/>                  |
| [**GetRange**](/windows/desktop/api/tapi3if/nf-tapi3if-itasrterminalevent-get_terminal) | Obtiene el intervalo de valores válidos para una [propiedad de dispositivo de audio](audiodeviceproperty.md)determinada.<br/> |
| [**Conjunto**](/windows/desktop/api/tapi3if/nf-tapi3if-itasrterminalevent-get_error)         | Establece el valor de una [propiedad de dispositivo de audio](audiodeviceproperty.md)determinada.<br/>                  |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|--------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3,1<br/>                                                         |
| Encabezado<br/>       | <dl> <dt>Ipmsp. h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>UUID. lib</dt> </dl>  |
| Archivo DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[IPConf MSP](ipconf-msp.md)
</dt> </dl>

 

