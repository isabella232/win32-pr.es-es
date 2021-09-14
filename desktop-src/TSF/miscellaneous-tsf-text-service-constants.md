---
title: Constantes misceláneas del servicio de texto TSF (Ctffunc.h)
description: Los siguientes valores se usan con servicios de texto.
ms.assetid: 38110314-1638-4963-92b6-4ba2f81fb7c2
topic_type:
- apiref
api_name:
- TF_MENUREADY
- TF_PROPUI_STATUS_SAVETOFILE
api_location:
- Ctffunc.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7ebd7d22f9cfbd59f95ee3dcfe68229536503b0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127170734"
---
# <a name="miscellaneous-tsf-text-service-constants"></a>Constantes misceláneas del servicio de texto TSF

Los siguientes valores se usan con servicios de texto.



| Constante o valor                                                                                                                                                                                                                                                            | Descripción                                                                                                                                                                                                                                                                              |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TF_MENUREADY"></span><span id="tf_menuready"></span><dl> <dt>**TF \_ MENUREADY**</dt> <dt>0x00000001</dt> </dl>                                                | No se usa actualmente.<br/>                                                                                                                                                                                                                                                           |
| <span id="TF_PROPUI_STATUS_SAVETOFILE"></span><span id="tf_propui_status_savetofile"></span><dl> <dt>**TF \_ PROPUI \_ STATUS \_ SAVETOFILE**</dt> <dt>0x00000001</dt> </dl> | La propiedad se puede serializar. Si este valor no está presente, la propiedad no se puede serializar. Este valor se usa con [ITfFnPropertyUIStatus::GetStatus](/windows/desktop/api/Ctffunc/nf-ctffunc-itffnpropertyuistatus-getstatus) e [ITfFnPropertyUIStatus::SetStatus](/windows/desktop/api/Ctffunc/nf-ctffunc-itffnpropertyuistatus-setstatus).<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                             |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                   |
| Redistribuible<br/>          | TSF 1.0 en Windows 2000 Professional<br/>                                        |
| Encabezado<br/>                   | <dl> <dt>Ctffunc.h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Ctffunc.idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ITfFnPropertyUIStatus::GetStatus](/windows/desktop/api/Ctffunc/nf-ctffunc-itffnpropertyuistatus-getstatus)
</dt> <dt>

[ITfFnPropertyUIStatus::SetStatus](/windows/desktop/api/Ctffunc/nf-ctffunc-itffnpropertyuistatus-setstatus)
</dt> </dl>

 

 





