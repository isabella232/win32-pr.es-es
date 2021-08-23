---
description: La interfaz ITCallQualityControl expone métodos que permiten a una aplicación obtener y establecer parámetros para el control de calidad de llamadas.
ms.assetid: 8d33e3b2-6af9-4c2d-bc65-905467f4fc6a
title: Interfaz ITCallQualityControl (Ipmsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5cb31452f6f4693e8bfbf725a5ddae7d7305868c2603806895c98e16df4d3e86
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119061013"
---
# <a name="itcallqualitycontrol-interface"></a>Interfaz ITCallQualityControl

\[Esta interfaz no está disponible para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente RTC proporciona una funcionalidad similar.\]

La **interfaz ITCallQualityControl** expone métodos que permiten a una aplicación obtener y establecer parámetros para el control de calidad de llamadas.

Esta interfaz se implementa mediante el [MSP de IPConf](ipconf-msp.md) y el [MSP H323](h323-msp.md). Solo se expone cuando una llamada usa estos proveedores de servicios.

## <a name="members"></a>Miembros

La **interfaz ITCallQualityControl** hereda de la [**interfaz IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **ITCallQualityControl** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz ITCallQualityControl** tiene estos métodos.



| Método                                            | Descripción                                                                                                     |
|:--------------------------------------------------|:----------------------------------------------------------------------------------------------------------------|
| [**Obtener**](itcallqualitycontrol-get.md)           | Obtiene el valor de una propiedad de [control de calidad de llamada determinada.](callqualityproperty.md)<br/>                  |
| [**GetRange**](itcallqualitycontrol-getrange.md) | Obtiene el intervalo de valores válidos para una propiedad [de control de calidad de llamada determinada.](callqualityproperty.md)<br/> |
| [**Establecer**](itcallqualitycontrol-set.md)           | Establece el valor de una propiedad de [control de calidad de llamada determinada.](callqualityproperty.md)<br/>                  |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|--------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3.1<br/>                                                         |
| Header<br/>       | <dl> <dt>Ipmsp.h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>Uuid.lib</dt> </dl>  |
| Archivo DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl> |



 

