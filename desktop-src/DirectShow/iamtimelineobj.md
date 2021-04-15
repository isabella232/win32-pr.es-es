---
description: La interfaz IAMTimelineObj proporciona métodos para manipular objetos Timeline en los servicios de edición de DirectShow (DES).
ms.assetid: ae8a778d-00b3-4b88-98dd-16e0a8645127
title: Interfaz IAMTimelineObj (QEDIT. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e968ec01d937aeac9a5838b75462a6d23a632512
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690158"
---
# <a name="iamtimelineobj-interface"></a>Interfaz IAMTimelineObj

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

La `IAMTimelineObj` interfaz proporciona métodos para manipular objetos Timeline en los [servicios de edición de DirectShow](directshow-editing-services.md) (des). Todos los objetos Timeline implementan este método, incluidos los objetos de origen, efecto, transición, pista, grupo y composición. Cree un objeto Timeline llamando al método [**IAMTimeline:: CreateEmptyNode**](iamtimeline-createemptynode.md) .

## <a name="members"></a>Miembros

La interfaz **IAMTimelineObj** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IAMTimelineObj** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **IAMTimelineObj** tiene estos métodos.



| Método                                                          | Descripción                                                                                                                            |
|:----------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------|
| [**ClearDirty**](iamtimelineobj-cleardirty.md)                 | No se admite.<br/>                                                                                                              |
| [**FixTimes**](iamtimelineobj-fixtimes.md)                     | Redondea las horas de inicio y detención especificadas a los límites del marco más cercano.<br/>                                                  |
| [**FixTimes2**](iamtimelineobj-fixtimes2.md)                   | Redondea las horas de inicio y detención especificadas, especificadas como valores de [**REFTIME**](reftime.md) , a los límites de fotogramas más cercanos.<br/> |
| [**GetDirtyRange**](iamtimelineobj-getdirtyrange.md)           | No se admite.<br/>                                                                                                              |
| [**GetDirtyRange2**](iamtimelineobj-getdirtyrange2.md)         | No se admite.<br/>                                                                                                              |
| [**GetEmbedDepth**](iamtimelineobj-getembeddepth.md)           | No se admite.<br/>                                                                                                              |
| [**GetGenID**](iamtimelineobj-getgenid.md)                     | Recupera el identificador generado del objeto.<br/>                                                                                |
| [**GetGroupIBelongTo**](iamtimelineobj-getgroupibelongto.md)   | No se admite.<br/>                                                                                                              |
| [**GetLocked**](iamtimelineobj-getlocked.md)                   | Recupera el estado de edición del objeto (bloqueado o desbloqueado).<br/>                                                                  |
| [**GetMuted**](iamtimelineobj-getmuted.md)                     | Recupera el estado silenciado del objeto.<br/>                                                                                         |
| [**GetPropertySetter**](iamtimelineobj-getpropertysetter.md)   | Recupera el establecedor de propiedad del objeto.<br/>                                                                                     |
| [**GetStartStop**](iamtimelineobj-getstartstop.md)             | Recupera las horas de inicio y detención del objeto, en relación con el elemento primario del objeto.<br/>                                               |
| [**GetStartStop2**](iamtimelineobj-getstartstop2.md)           | Recupera las horas de inicio y detención del objeto, como valores [**REFTIME**](reftime.md) .<br/>                                          |
| [**GetSubObject**](iamtimelineobj-getsubobject.md)             | Recupera el subobjeto asociado a este objeto.<br/>                                                                        |
| [**GetSubObjectGUID**](iamtimelineobj-getsubobjectguid.md)     | Recupera el GUID del subobjeto asociado a este objeto Timeline.<br/>                                                   |
| [**GetSubObjectGUIDB**](iamtimelineobj-getsubobjectguidb.md)   | Recupera el GUID del subobjeto como un valor **BSTR** .<br/>                                                                    |
| [**GetSubObjectLoaded**](iamtimelineobj-getsubobjectloaded.md) | Determina si se ha establecido el puntero de subobjeto del objeto.<br/>                                                             |
| [**GetTimelineNoRef**](iamtimelineobj-gettimelinenoref.md)     | No se admite.<br/>                                                                                                              |
| [**GetTimelineType**](iamtimelineobj-gettimelinetype.md)       | Recupera el tipo del objeto.<br/>                                                                                                |
| [**GetUserData**](iamtimelineobj-getuserdata.md)               | Recupera los datos persistentes definidos por la aplicación.<br/>                                                                          |
| [**GetUserID**](iamtimelineobj-getuserid.md)                   | Recupera el identificador definido por la aplicación del objeto.<br/>                                                                      |
| [**GetUserName**](iamtimelineobj-getusername.md)               | Recupera el nombre definido por la aplicación del objeto.<br/>                                                                            |
| [**Retirar**](iamtimelineobj-remove.md)                         | Quita este objeto de la escala de tiempo, para volver a insertarlo en otro lugar.<br/>                                                           |
| [**RemoveAll**](iamtimelineobj-removeall.md)                   | Quita de forma permanente este objeto de la escala de tiempo, incluidos los subobjetos y secundarios.<br/>                                       |
| [**SetDirtyRange**](iamtimelineobj-setdirtyrange.md)           | Sin implementar.<br/>                                                                                                            |
| [**SetDirtyRange2**](iamtimelineobj-setdirtyrange2.md)         | Sin implementar.<br/>                                                                                                            |
| [**SetLocked**](iamtimelineobj-setlocked.md)                   | Establece el estado de edición del objeto en bloqueado o desbloqueado.<br/>                                                                      |
| [**SetMuted**](iamtimelineobj-setmuted.md)                     | Establece el estado silenciado del objeto.<br/>                                                                                              |
| [**SetPropertySetter**](iamtimelineobj-setpropertysetter.md)   | Establece el establecedor de propiedad del objeto.<br/>                                                                                          |
| [**SetStartStop**](iamtimelineobj-setstartstop.md)             | Establece las horas de inicio y detención del objeto, en relación con la escala de tiempo.<br/>                                                           |
| [**SetStartStop2**](iamtimelineobj-setstartstop2.md)           | Establece las horas de inicio y detención del objeto, como valores **REFTIME** .<br/>                                                              |
| [**SetSubObject**](iamtimelineobj-setsubobject.md)             | No se admite.<br/>                                                                                                              |
| [**SetSubObjectGUID**](iamtimelineobj-setsubobjectguid.md)     | Especifica el identificador único global (GUID) del subobjeto asociado a este objeto.<br/>                               |
| [**SetSubObjectGUIDB**](iamtimelineobj-setsubobjectguidb.md)   | Especifica el GUID del subobjeto como un valor **BSTR** .<br/>                                                                    |
| [**SetTimelineType**](iamtimelineobj-settimelinetype.md)       | No se admite.<br/>                                                                                                              |
| [**SetUserData**](iamtimelineobj-setuserdata.md)               | Establece los datos persistentes definidos por la aplicación.<br/>                                                                                   |
| [**SetUserID**](iamtimelineobj-setuserid.md)                   | Establece un identificador definido por la aplicación para el objeto.<br/>                                                                      |
| [**SetUserName**](iamtimelineobj-setusername.md)               | Establece un nombre definido por la aplicación para el objeto.<br/>                                                                            |



 

## <a name="remarks"></a>Observaciones

> [!Note]  
> El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.

 

> [!Note]  
> Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>QEDIT. h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



 

 
