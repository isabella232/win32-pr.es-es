---
title: Códigos de error (UIAutomationCoreApi.h)
description: En este tema se describen los códigos de error expuestos por Microsoft Automatización de la interfaz de usuario.
ms.assetid: f7820aa3-908e-426e-851c-84397019d735
topic_type:
- apiref
api_name:
- UIA_E_ELEMENTNOTAVAILABLE
- UIA_E_ELEMENTNOTENABLED
- UIA_E_INVALIDOPERATION
- UIA_E_NOCLICKABLEPOINT
- UIA_E_NOTSUPPORTED
- UIA_E_PROXYASSEMBLYNOTLOADED
- UIA_E_TIMEOUT
api_location:
- UIAutomationCoreApi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: baaa03746bfb1a5e56fcac8b39d326581159f459
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127070534"
---
# <a name="error-codes-uiautomationcoreapih"></a>Códigos de error (UIAutomationCoreApi.h)

En este tema se describen los códigos de error expuestos por Microsoft Automatización de la interfaz de usuario. La lista se ordena alfabéticamente por nombre.



| Constante o valor                                                                                                                                                                                                                                                              | Descripción                                                                                                                                                                                                                                              |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="UIA_E_ELEMENTNOTAVAILABLE"></span><span id="uia_e_elementnotavailable"></span><dl> <dt>**UIA \_ E \_ ELEMENTNOTAVAILABLE**</dt> <dt>0x80040201</dt> </dl>          | Indica que se llamó a un método en un elemento virtualizado o en un elemento que ya no existe, normalmente porque se ha destruido. <br/>                                                                                                  |
| <span id="UIA_E_ELEMENTNOTENABLED"></span><span id="uia_e_elementnotenabled"></span><dl> <dt>**UIA \_ E \_ ELEMENTNOTENABLED**</dt> <dt>0x80040200</dt> </dl>                | Indica que se llamó a un método que requiere un elemento habilitado, como [**Select**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-select) o [**Expand,**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-expand)en un elemento deshabilitado. <br/>             |
| <span id="UIA_E_INVALIDOPERATION"></span><span id="uia_e_invalidoperation"></span><dl> <dt>**UIA \_ E \_ INVALIDOPERATION**</dt> <dt>0x80131509</dt> </dl>                   | Indica que el método intentó una operación que no era válida.<br/>                                                                                                                                                                          |
| <span id="UIA_E_NOCLICKABLEPOINT"></span><span id="uia_e_noclickablepoint"></span><dl> <dt>**UIA \_ E \_ NOCLICKABLEPOINT**</dt> <dt>0x80040202</dt> </dl>                   | Indica que se [**llamó al método GetClickablePoint**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getclickablepoint) en un elemento que no tiene ningún punto en el que se pueda hacer clic.<br/>                                                                                    |
| <span id="UIA_E_NOTSUPPORTED"></span><span id="uia_e_notsupported"></span><dl> <dt>**UIA \_ E \_ NOTSUPPORTED**</dt> <dt>0x80040204</dt> </dl>                               | Indica que el proveedor no admite explícitamente la propiedad o el patrón de control especificados. Automatización de la interfaz de usuario devolverá este código de error al autor de la llamada sin intentar proporcionar un valor predeterminado o volver a otro proveedor.<br/> |
| <span id="UIA_E_PROXYASSEMBLYNOTLOADED"></span><span id="uia_e_proxyassemblynotloaded"></span><dl> <dt>**UIA \_ E \_ PROXYASSEMBLYNOTLOADED**</dt> <dt>0x80040203</dt> </dl> | Indica que se produjo un problema al cargar un ensamblado que contiene un proveedor del lado cliente (proxy).<br/>                                                                                                                                      |
| <span id="UIA_E_TIMEOUT"></span><span id="uia_e_timeout"></span><dl> <dt>**UIA \_ E \_ TIMEOUT**</dt> <dt>0x80131505</dt> </dl>                                                      | Indica que ha expirado el tiempo asignado para un proceso o una operación.<br/>                                                                                                                                                                      |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>                                                      |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                             |
| Encabezado<br/>                   | <dl> <dt>UIAutomationCoreApi.h</dt> </dl> |



 

 





