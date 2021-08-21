---
description: ITStreamQualityControl expone métodos que permiten a una aplicación obtener y establecer parámetros para el control de calidad de flujo.
ms.assetid: b9ecf24a-c87e-44a6-9e20-aa7bf7619314
title: Interfaz ITStreamQualityControl (Ipmsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d4af57228cc7a91dad8232648d973d36a700b713d787f486e9f4a380bca6f6e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118863900"
---
# <a name="itstreamqualitycontrol-interface"></a>Interfaz ITStreamQualityControl

\[Esta interfaz no está disponible para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente RTC proporciona una funcionalidad similar.\]

**ITStreamQualityControl expone métodos** que permiten a una aplicación obtener y establecer parámetros para el control de calidad del flujo.

Esta interfaz se implementa mediante el [MSP de IPConf](ipconf-msp.md) y [el MSP H323](h323-msp.md). Solo se expone cuando una llamada usa estos proveedores de servicios.

## <a name="members"></a>Miembros

La **interfaz ITStreamQualityControl** hereda de [**la interfaz IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **ITStreamQualityControl también** tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz ITStreamQualityControl** tiene estos métodos.



| Método                                              | Descripción                                                                                                 |
|:----------------------------------------------------|:------------------------------------------------------------------------------------------------------------|
| [**Obtener**](itstreamqualitycontrol-get.md)           | Obtiene el valor de una propiedad de [calidad de flujo determinada.](streamqualityproperty.md)<br/>                  |
| [**GetRange**](itstreamqualitycontrol-getrange.md) | Obtiene el intervalo de valores válidos para una propiedad [de calidad de flujo determinada.](streamqualityproperty.md)<br/> |
| [**Establecer**](itstreamqualitycontrol-set.md)           | Establece el valor de una propiedad de [calidad de flujo determinada.](streamqualityproperty.md)<br/>                  |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|--------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3.1<br/>                                                         |
| Header<br/>       | <dl> <dt>Ipmsp.h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>Uuid.lib</dt> </dl>  |
| Archivo DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl> |



 

