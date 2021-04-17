---
description: 'Marcas usadas por los métodos IWiaDevMgr:: GetImageDlg, IWiaDevMgr2:: GetImageDlg, IWiaItem::D eviceDlg y IWiaItem2::D eviceDlg para controlar la operación del cuadro de diálogo.'
ms.assetid: 468a3c9e-64f8-456d-aad9-fa7c6876fbe6
title: WiaFlag (Wiadef. h)
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
ms.openlocfilehash: c906f22e168ca29aadd2e9450fac6225c8b91c17
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659805"
---
# <a name="wiaflag"></a>WiaFlag

Marcas usadas por los métodos [**IWiaDevMgr:: GetImageDlg**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-getimagedlg), [**IWiaDevMgr2:: GetImageDlg**](-wia-iwiadevmgr2-getimagedlg.md), [**IWiaItem::D eviceDlg**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-devicedlg)y [**IWiaItem2::D evicedlg**](-wia-iwiaitem2-devicedlg.md) para controlar la operación del cuadro de diálogo.



| Constante                                                                                                                                                                                                                | Descripción                                                                                                                                                                                                 |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WIA_DEVICE_DIALOG_SINGLE_IMAGE"></span><span id="wia_device_dialog_single_image"></span><dl> <dt>**\_cuadro de diálogo de dispositivo WIA \_ \_ \_ imagen única**</dt> </dl>     | Restrinja la selección de imágenes a una sola imagen en el cuadro de diálogo adquisición de imagen de dispositivo.<br/>                                                                                                           |
| <span id="WIA_DEVICE_DIALOG_USE_COMMON_UI"></span><span id="wia_device_dialog_use_common_ui"></span><dl> <dt>**cuadro de diálogo de dispositivo WIA uso de la \_ \_ interfaz de \_ \_ \_ usuario común**</dt> </dl> | Use la interfaz de usuario del sistema, si está disponible, en lugar de la interfaz de usuario proporcionada por el proveedor. Si la interfaz de usuario del sistema no está disponible, se usa la interfaz de usuario del proveedor. Si no hay ninguna interfaz de usuario disponible, la función devuelve E \_ NOTIMPL.<br/>      |
| <span id="WIA_SELECT_DEVICE_NODEFAULT"></span><span id="wia_select_device_nodefault"></span><dl> <dt>**WIA \_ seleccionar \_ dispositivo \_ predeterminado**</dt> </dl>               | Fuerce el método [**IWiaDevMgr:: GetImageDlg**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-getimagedlg) o [**IWiaDevMgr2:: GetImageDlg**](-wia-iwiadevmgr2-getimagedlg.md) para mostrar el cuadro de diálogo **seleccionar dispositivo** .<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]<br/>              |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Wiadef. h</dt> </dl> |



 

 




