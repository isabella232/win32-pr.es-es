---
description: La interfaz ITCallQualityControl expone métodos que permiten a una aplicación obtener y establecer parámetros para el control de calidad de llamadas.
ms.assetid: 8d33e3b2-6af9-4c2d-bc65-905467f4fc6a
title: Interfaz ITCallQualityControl (Ipmsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 447e2f34db76ba15ecaec9e7bc03a0d2d398c493
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680209"
---
# <a name="itcallqualitycontrol-interface"></a>Interfaz ITCallQualityControl

\[ Esta interfaz no está disponible para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente de RTC proporciona una funcionalidad similar.\]

La interfaz **ITCallQualityControl** expone métodos que permiten a una aplicación obtener y establecer parámetros para el control de calidad de llamadas.

Esta interfaz la implementa [IPCONF MSP](ipconf-msp.md) y el MSP de [H323](h323-msp.md). Solo se expone cuando una llamada utiliza estos proveedores de servicios.

## <a name="members"></a>Miembros

La interfaz **ITCallQualityControl** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **ITCallQualityControl** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **ITCallQualityControl** tiene estos métodos.



| Método                                            | Descripción                                                                                                     |
|:--------------------------------------------------|:----------------------------------------------------------------------------------------------------------------|
| [**Obtener**](itcallqualitycontrol-get.md)           | Obtiene el valor de una [propiedad de control de calidad de llamada](callqualityproperty.md)determinada.<br/>                  |
| [**GetRange**](itcallqualitycontrol-getrange.md) | Obtiene el intervalo de valores válidos para una [propiedad de control de calidad de llamada](callqualityproperty.md)determinada.<br/> |
| [**Conjunto**](itcallqualitycontrol-set.md)           | Establece el valor de una [propiedad de control de calidad de llamada](callqualityproperty.md)determinada.<br/>                  |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|--------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3,1<br/>                                                         |
| Encabezado<br/>       | <dl> <dt>Ipmsp. h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>UUID. lib</dt> </dl>  |
| Archivo DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl> |



 

