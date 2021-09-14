---
description: La interfaz IAMTimelineObj proporciona métodos para manipular objetos de escala de tiempo en DirectShow Editing Services (DES).
ms.assetid: ae8a778d-00b3-4b88-98dd-16e0a8645127
title: Interfaz IAMTimelineObj (Qedit.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061632"
---
# <a name="iamtimelineobj-interface"></a>Interfaz IAMTimelineObj

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

La `IAMTimelineObj` interfaz proporciona métodos para manipular objetos de escala de tiempo [DirectShow Editing Services](directshow-editing-services.md) (DES). Todos los objetos de escala de tiempo implementan este método, incluidos los objetos de origen, efecto, transición, seguimiento, grupo y composición. Cree un objeto de escala de tiempo llamando al [**método IAMTimeline::CreateEmptyNode.**](iamtimeline-createemptynode.md)

## <a name="members"></a>Members

La **interfaz IAMTimelineObj** hereda de la [**interfaz IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IAMTimelineObj** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IAMTimelineObj** tiene estos métodos.



| Método                                                          | Descripción                                                                                                                            |
|:----------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------|
| [**ClearDirty**](iamtimelineobj-cleardirty.md)                 | No compatible.<br/>                                                                                                              |
| [**FixTimes**](iamtimelineobj-fixtimes.md)                     | Redondea las horas de inicio y de detenerse especificadas a los límites de fotograma más cercanos.<br/>                                                  |
| [**FixTimes2**](iamtimelineobj-fixtimes2.md)                   | Redondea las horas de inicio y de detenerse especificadas, especificadas como [**valores REFTIME,**](reftime.md) a los límites de fotograma más cercanos.<br/> |
| [**GetDirtyRange**](iamtimelineobj-getdirtyrange.md)           | No compatible.<br/>                                                                                                              |
| [**GetDirtyRange2**](iamtimelineobj-getdirtyrange2.md)         | No compatible.<br/>                                                                                                              |
| [**GetEmbedDepth**](iamtimelineobj-getembeddepth.md)           | No compatible.<br/>                                                                                                              |
| [**GetGenID**](iamtimelineobj-getgenid.md)                     | Recupera el identificador generado del objeto.<br/>                                                                                |
| [**GetGroupIBelongTo**](iamtimelineobj-getgroupibelongto.md)   | No compatible.<br/>                                                                                                              |
| [**GetLocked**](iamtimelineobj-getlocked.md)                   | Recupera el estado de edición del objeto (bloqueado o desbloqueado).<br/>                                                                  |
| [**GetMuted**](iamtimelineobj-getmuted.md)                     | Recupera el estado muted del objeto.<br/>                                                                                         |
| [**GetPropertySetter**](iamtimelineobj-getpropertysetter.md)   | Recupera el setter de propiedad del objeto.<br/>                                                                                     |
| [**GetStartStop**](iamtimelineobj-getstartstop.md)             | Recupera las horas de inicio y de detenerse del objeto, en relación con el elemento primario del objeto.<br/>                                               |
| [**GetStartStop2**](iamtimelineobj-getstartstop2.md)           | Recupera las horas de inicio y de detenerse del objeto, como [**valores REFTIME.**](reftime.md)<br/>                                          |
| [**GetSubObject**](iamtimelineobj-getsubobject.md)             | Recupera el subobjeto asociado a este objeto .<br/>                                                                        |
| [**GetSubObjectGUID**](iamtimelineobj-getsubobjectguid.md)     | Recupera el GUID del subobjeto asociado a este objeto de escala de tiempo.<br/>                                                   |
| [**GetSubObjectGUIDB**](iamtimelineobj-getsubobjectguidb.md)   | Recupera el GUID del subobjeto como un **valor BSTR.**<br/>                                                                    |
| [**GetSubObjectLoaded**](iamtimelineobj-getsubobjectloaded.md) | Determina si se ha establecido el puntero del subobjeto del objeto.<br/>                                                             |
| [**GetTimelineNoRef**](iamtimelineobj-gettimelinenoref.md)     | No compatible.<br/>                                                                                                              |
| [**GetTimelineType**](iamtimelineobj-gettimelinetype.md)       | Recupera el tipo del objeto.<br/>                                                                                                |
| [**GetUserData**](iamtimelineobj-getuserdata.md)               | Recupera los datos persistentes definidos por la aplicación.<br/>                                                                          |
| [**GetUserID**](iamtimelineobj-getuserid.md)                   | Recupera el identificador definido por la aplicación del objeto.<br/>                                                                      |
| [**GetUserName**](iamtimelineobj-getusername.md)               | Recupera el nombre definido por la aplicación del objeto.<br/>                                                                            |
| [**Remove**](iamtimelineobj-remove.md)                         | Quita este objeto de la escala de tiempo, para su reinserción en otro lugar.<br/>                                                           |
| [**Removeall**](iamtimelineobj-removeall.md)                   | Quita permanentemente este objeto de la escala de tiempo, incluidos los subobjetos y los elementos secundarios.<br/>                                       |
| [**SetDirtyRange**](iamtimelineobj-setdirtyrange.md)           | Sin implementar.<br/>                                                                                                            |
| [**SetDirtyRange2**](iamtimelineobj-setdirtyrange2.md)         | Sin implementar.<br/>                                                                                                            |
| [**SetLocked**](iamtimelineobj-setlocked.md)                   | Establece el estado de edición del objeto en bloqueado o desbloqueado.<br/>                                                                      |
| [**SetMuted**](iamtimelineobj-setmuted.md)                     | Establece el estado muted del objeto.<br/>                                                                                              |
| [**SetPropertySetter**](iamtimelineobj-setpropertysetter.md)   | Establece el establecedor de propiedades del objeto.<br/>                                                                                          |
| [**SetStartStop**](iamtimelineobj-setstartstop.md)             | Establece las horas de inicio y de detenerse del objeto, en relación con la escala de tiempo.<br/>                                                           |
| [**SetStartStop2**](iamtimelineobj-setstartstop2.md)           | Establece las horas de inicio y de detenerse del objeto, como **valores REFTIME.**<br/>                                                              |
| [**SetSubObject**](iamtimelineobj-setsubobject.md)             | No compatible.<br/>                                                                                                              |
| [**SetSubObjectGUID**](iamtimelineobj-setsubobjectguid.md)     | Especifica el identificador único global (GUID) del subobjeto asociado a este objeto.<br/>                               |
| [**SetSubObjectGUIDB**](iamtimelineobj-setsubobjectguidb.md)   | Especifica el GUID del subobjeto como un **valor BSTR.**<br/>                                                                    |
| [**SetTimelineType**](iamtimelineobj-settimelinetype.md)       | No compatible.<br/>                                                                                                              |
| [**SetUserData**](iamtimelineobj-setuserdata.md)               | Establece los datos persistentes definidos por la aplicación.<br/>                                                                                   |
| [**SetUserID**](iamtimelineobj-setuserid.md)                   | Establece un identificador definido por la aplicación para el objeto .<br/>                                                                      |
| [**SetUserName**](iamtimelineobj-setusername.md)               | Establece un nombre definido por la aplicación para el objeto .<br/>                                                                            |



 

## <a name="remarks"></a>Observaciones

> [!Note]  
> El archivo de encabezado Qedit.h no es compatible con los encabezados de Direct3D posteriores a la versión 7.

 

> [!Note]  
> Para obtener Qedit.h, descargue la actualización del SDK de [Microsoft Windows para Windows Vista y .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit.h no está disponible en el SDK de Microsoft Windows para Windows 7 y .NET Framework 3.5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



 

 
