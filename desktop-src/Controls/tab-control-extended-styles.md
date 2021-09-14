---
title: Estilos extendidos de control de pestañas (CommCtrl.h)
description: El control de pestaña ahora admite estilos extendidos. Estos estilos se manipulan mediante los mensajes \_ GETEXTENDEDSTYLE y TCM SETEXTENDEDSTYLE de TCM y no deben confundirse con los estilos de ventana extendidos que se pasan a \_ CreateWindowEx.
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127166942"
---
# <a name="tab-control-extended-styles"></a>Estilos extendidos de control de pestañas

El control de pestaña ahora admite estilos extendidos. Estos estilos se manipulan mediante los mensajes [**\_ GETEXTENDEDSTYLE**](tcm-getextendedstyle.md) y [**\_ TCM SETEXTENDEDSTYLE**](tcm-setextendedstyle.md) de TCM y no deben confundirse con los estilos de ventana extendidos que se pasan a [**CreateWindowEx.**](/windows/desktop/api/winuser/nf-winuser-createwindowexa)



| Constante                                                                                                                                                                               | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TCS_EX_FLATSEPARATORS"></span><span id="tcs_ex_flatseparators"></span><dl> <dt>**TCS \_ EX \_ FLATSEPARATORS**</dt> </dl> | [Versión 4.71.](common-control-versions.md) El control de ficha dibujará separadores entre los elementos de ficha. Este estilo extendido solo afecta a los controles de ficha que tienen los [**estilos TCS \_ BUTTONS**](tab-control-styles.md) y [**TCS \_ FLATBUTTONS.**](tab-control-styles.md) De forma predeterminada, la creación del control de pestaña **con el estilo \_ FLATBUTTONS** de TCS establece este estilo extendido. Si no necesita separadores, debe quitar este estilo extendido después de crear el control.<br/> |
| <span id="TCS_EX_REGISTERDROP"></span><span id="tcs_ex_registerdrop"></span><dl> <dt>**TCS \_ EX \_ REGISTERDROP**</dt> </dl>       | [Versión 4.71.](common-control-versions.md) El control de pestaña genera códigos [de notificación \_ GETOBJECT](tcn-getobject.md) de TCN para solicitar un objeto de destino de colocación cuando se arrastra un objeto sobre los elementos de tabulación del control. La aplicación debe llamar [**a CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize) o [**OleInitialize antes**](/windows/desktop/api/ole2/nf-ole2-oleinitialize) de establecer este estilo. <br/>                                                                                                                                               |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>CommCtrl.h</dt> </dl> |



 

