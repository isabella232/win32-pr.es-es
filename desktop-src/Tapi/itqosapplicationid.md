---
description: La interfaz ITQOSApplicationID expone un método que permite a una aplicación obtener el identificador de QOS para la llamada actual.
ms.assetid: 1df50b3a-bd16-4e9b-afca-b025bfe537a4
title: Interfaz ITQOSApplicationID (Ipmsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d4067d7a476e2a402c278b22dcee21b6542919396178350e73017d56ba92258
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120126285"
---
# <a name="itqosapplicationid-interface"></a>Interfaz ITQOSApplicationID

\[Esta interfaz no está disponible para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente RTC proporciona una funcionalidad similar.\]

La **interfaz ITQOSApplicationID** expone un método que permite a una aplicación obtener el identificador de QOS para la llamada actual.

El MSP de [IPConf](ipconf-msp.md) implementa esta interfaz y solo se expone cuando una llamada usa la conferencia IP.

## <a name="members"></a>Miembros

La **interfaz ITQOSApplicationID** hereda de la [**interfaz IDispatch.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) **ITQOSApplicationID** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz ITQOSApplicationID** tiene estos métodos.



| Método                                                                | Descripción                         |
|:----------------------------------------------------------------------|:------------------------------------|
| [**SetQOSApplicationID**](itqosapplicationid-setqosapplicationid.md) | Establece el identificador de QOS.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|--------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3.1<br/>                                                         |
| Header<br/>       | <dl> <dt>Ipmsp.h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>Uuid.lib</dt> </dl>  |
| Archivo DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl> |



 

