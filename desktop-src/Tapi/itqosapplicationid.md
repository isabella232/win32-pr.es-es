---
description: La interfaz ITQOSApplicationID expone un método que permite a una aplicación obtener el identificador de QOS de la llamada actual.
ms.assetid: 1df50b3a-bd16-4e9b-afca-b025bfe537a4
title: Interfaz ITQOSApplicationID (Ipmsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23df8da80798cc52ecd73b4f29288812f3774d9f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681237"
---
# <a name="itqosapplicationid-interface"></a>Interfaz ITQOSApplicationID

\[ Esta interfaz no está disponible para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente de RTC proporciona una funcionalidad similar.\]

La interfaz **ITQOSApplicationID** expone un método que permite a una aplicación obtener el identificador de QoS de la llamada actual.

Esta interfaz se implementa mediante el [MSP de IPConf](ipconf-msp.md) y solo se expone cuando una llamada usa conferencias IP.

## <a name="members"></a>Miembros

La interfaz **ITQOSApplicationID** hereda de la interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **ITQOSApplicationID** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **ITQOSApplicationID** tiene estos métodos.



| Método                                                                | Descripción                         |
|:----------------------------------------------------------------------|:------------------------------------|
| [**SetQOSApplicationID**](itqosapplicationid-setqosapplicationid.md) | Establece el identificador de QOS.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|--------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3,1<br/>                                                         |
| Encabezado<br/>       | <dl> <dt>Ipmsp. h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>UUID. lib</dt> </dl>  |
| Archivo DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl> |



 

