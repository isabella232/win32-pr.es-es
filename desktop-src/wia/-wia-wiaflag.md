---
description: Marcas usadas por los métodos IWiaDevMgr::GetImageDlg, IWiaDevMgr2::GetImageDlg, IWiaItem::D eviceDlg e IWiaItem2::D eviceDlg para controlar la operación del cuadro de diálogo.
ms.assetid: 468a3c9e-64f8-456d-aad9-fa7c6876fbe6
title: WiaFlag (Wiadef.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WIA_DEVICE_DIALOG_SINGLE_IMAGE
- WIA_DEVICE_DIALOG_USE_COMMON_UI
- WIA_SELECT_DEVICE_NODEFAULT
api_type:
- HeaderDef
api_location:
- wiadef.h
ms.openlocfilehash: bfff3ccab0f8aa73c2ae6e34086c3abc909a4b4d8b9222bf4d6d8a86e0a36c57
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117668973"
---
# <a name="wiaflag"></a>WiaFlag

Marcas usadas por los métodos [**IWiaDevMgr::GetImageDlg**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-getimagedlg), [**IWiaDevMgr2::GetImageDlg,**](-wia-iwiadevmgr2-getimagedlg.md) [**IWiaItem::D eviceDlg**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-devicedlg)e [**IWiaItem2::D eviceDlg**](-wia-iwiaitem2-devicedlg.md) para controlar la operación del cuadro de diálogo.



| Constante                                                                                                                                                                                                                | Descripción                                                                                                                                                                                                 |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WIA_DEVICE_DIALOG_SINGLE_IMAGE"></span><span id="wia_device_dialog_single_image"></span><dl> <dt>**IMAGEN ÚNICA \_ DEL CUADRO DE DIÁLOGO DE DISPOSITIVO \_ \_ \_ WIA**</dt> </dl>     | Restrinja la selección de imágenes a una sola imagen en el cuadro de diálogo de adquisición de imágenes del dispositivo.<br/>                                                                                                           |
| <span id="WIA_DEVICE_DIALOG_USE_COMMON_UI"></span><span id="wia_device_dialog_use_common_ui"></span><dl> <dt>**CUADRO DE DIÁLOGO \_ DE DISPOSITIVO WIA \_ USAR INTERFAZ DE USUARIO \_ \_ \_ COMÚN**</dt> </dl> | Use la interfaz de usuario del sistema, si está disponible, en lugar de la interfaz de usuario proporcionada por el proveedor. Si la interfaz de usuario del sistema no está disponible, se usa la interfaz de usuario del proveedor. Si ninguna interfaz de usuario está disponible, la función devuelve E \_ NOTIMPL.<br/>      |
| <span id="WIA_SELECT_DEVICE_NODEFAULT"></span><span id="wia_select_device_nodefault"></span><dl> <dt>**WIA \_ SELECT \_ DEVICE \_ NODEFAULT**</dt> </dl>               | Fuerce [**al método IWiaDevMgr::GetImageDlg**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-getimagedlg) o [**IWiaDevMgr2::GetImageDlg**](-wia-iwiadevmgr2-getimagedlg.md) a mostrar el **cuadro de diálogo** Seleccionar dispositivo.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional, Windows aplicaciones de escritorio XP \[\]<br/>              |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                |
| Header<br/>                   | <dl> <dt>Wiadef.h</dt> </dl> |



 

 




