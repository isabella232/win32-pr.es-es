---
description: ITStreamQualityControl expone métodos que permiten a una aplicación obtener y establecer parámetros para el control de calidad de flujo.
ms.assetid: b9ecf24a-c87e-44a6-9e20-aa7bf7619314
title: Interfaz ITStreamQualityControl (Ipmsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98a85eccc907ef2c8f4c0b67c2a32244004dbdca
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073475"
---
# <a name="itstreamqualitycontrol-interface"></a>Interfaz ITStreamQualityControl

\[Esta interfaz no está disponible para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente RTC proporciona una funcionalidad similar.\]

**ITStreamQualityControl expone métodos** que permiten a una aplicación obtener y establecer parámetros para el control de calidad de flujo.

Esta interfaz se implementa mediante el [MSP de IPConf](ipconf-msp.md) y [el MSP H323](h323-msp.md). Solo se expone cuando una llamada usa estos proveedores de servicios.

## <a name="members"></a>Members

La **interfaz ITStreamQualityControl** hereda de la [**interfaz IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **ITStreamQualityControl también** tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz ITStreamQualityControl** tiene estos métodos.



| Método                                              | Descripción                                                                                                 |
|:----------------------------------------------------|:------------------------------------------------------------------------------------------------------------|
| [**Obtener**](itstreamqualitycontrol-get.md)           | Obtiene el valor de una propiedad de [calidad de flujo determinada.](streamqualityproperty.md)<br/>                  |
| [**GetRange**](itstreamqualitycontrol-getrange.md) | Obtiene el intervalo de valores válidos para una propiedad [de calidad de flujo determinada.](streamqualityproperty.md)<br/> |
| [**Set**](itstreamqualitycontrol-set.md)           | Establece el valor de una propiedad de [calidad de flujo determinada.](streamqualityproperty.md)<br/>                  |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|--------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3.1<br/>                                                         |
| Encabezado<br/>       | <dl> <dt>Ipmsp.h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>Uuid.lib</dt> </dl>  |
| Archivo DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl> |



 

