---
title: Estilos extendidos del control de pestaña (CommCtrl. h)
description: El control de pestaña ahora admite estilos extendidos. Estos estilos se manipulan mediante los \_ mensajes TCM GETEXTENDEDSTYLE y TCM \_ SETEXTENDEDSTYLE y no se deben confundir con los estilos de ventana extendidos que se pasan a CreateWindowEx.
ms.assetid: 24294037-598c-4fcd-8a7c-8647ccfb1d81
topic_type:
- apiref
api_name:
- TCS_EX_FLATSEPARATORS
- TCS_EX_REGISTERDROP
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c4e16b40a394bc9b808386d3cbdc3abf9b3d928
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649771"
---
# <a name="tab-control-extended-styles"></a>Estilos extendidos del control de pestaña

El control de pestaña ahora admite estilos extendidos. Estos estilos se manipulan mediante los mensajes [**TCM \_ GETEXTENDEDSTYLE**](tcm-getextendedstyle.md) y [**TCM \_ SETEXTENDEDSTYLE**](tcm-setextendedstyle.md) y no se deben confundir con los estilos de ventana extendidos que se pasan a [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa).



| Constante                                                                                                                                                                               | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TCS_EX_FLATSEPARATORS"></span><span id="tcs_ex_flatseparators"></span><dl> <dt>**ECT \_ ex \_ FLATSEPARATORS**</dt> </dl> | [Versión 4,71](common-control-versions.md). El control de pestaña dibujará separadores entre los elementos de ficha. Este estilo extendido solo afecta a los controles de ficha que tienen los [**\_ botones de TCS**](tab-control-styles.md) y los estilos de [**\_ FLATBUTTONS de TCS**](tab-control-styles.md) . De forma predeterminada, al crear el control de pestaña con el estilo **TCS \_ FLATBUTTONS** se establece este estilo extendido. Si no necesita separadores, debe quitar este estilo extendido después de crear el control.<br/> |
| <span id="TCS_EX_REGISTERDROP"></span><span id="tcs_ex_registerdrop"></span><dl> <dt>**ECT \_ ex \_ REGISTERDROP**</dt> </dl>       | [Versión 4,71](common-control-versions.md). El control de pestaña genera códigos de notificación [TCN \_ GETOBJECT](tcn-getobject.md) para solicitar un objeto de destino de colocación cuando se arrastra un objeto sobre los elementos de ficha del control. La aplicación debe llamar a [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize) o [**OleInitialize**](/windows/desktop/api/ole2/nf-ole2-oleinitialize) antes de establecer este estilo. <br/>                                                                                                                                               |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>CommCtrl. h</dt> </dl> |



 

