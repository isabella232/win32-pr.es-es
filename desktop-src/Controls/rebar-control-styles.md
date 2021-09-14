---
title: Estilos de control Rebar (CommCtrl.h)
description: Los controles rebar admiten una variedad de estilos de control además de los estilos de ventana estándar.
ms.assetid: 9690a4bd-51bd-4df9-8988-7da3ece7899f
topic_type:
- apiref
api_name:
- RBS_AUTOSIZE
- RBS_BANDBORDERS
- RBS_DBLCLKTOGGLE
- RBS_FIXEDORDER
- RBS_REGISTERDROP
- RBS_TOOLTIPS
- RBS_VARHEIGHT
- RBS_VERTICALGRIPPER
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67b9f447df2cbf1bb2b956a7ec300d1f29280eef
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127167181"
---
# <a name="rebar-control-styles"></a>Estilos de control Rebar

Los controles rebar admiten una variedad de estilos de control además de los estilos de ventana estándar.



| Constante                                                                                                                                                                        | Descripción                                                                                                                                                                                                                                                                                                                                                 |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RBS_AUTOSIZE"></span><span id="rbs_autosize"></span><dl> <dt>**RBS \_ AUTOSIZE**</dt> </dl>                      | [Versión 4.71.](common-control-versions.md) El control rebar cambiará automáticamente el diseño de las bandas cuando cambie el tamaño o la posición del control. Cuando esto ocurra, se enviará una notificación [ \_ RBN AUTOSIZE.](rbn-autosize.md)<br/>                                                                                              |
| <span id="RBS_BANDBORDERS"></span><span id="rbs_bandborders"></span><dl> <dt>**RBS \_ BANDBORDERS**</dt> </dl>             | [Versión 4.71.](common-control-versions.md) El control rebar muestra líneas estrechas para separar bandas adyacentes.<br/>                                                                                                                                                                                                                                 |
| <span id="RBS_DBLCLKTOGGLE"></span><span id="rbs_dblclktoggle"></span><dl> <dt>**RBS \_ DBLCLKTOGGLE**</dt> </dl>          | [Versión 4.71.](common-control-versions.md) La banda de rebar alternará su estado maximizado o minimizado cuando el usuario haga doble clic en la banda. Sin este estilo, el estado maximizado o minimizado se alterna cuando el usuario hace clic en la banda.<br/>                                                                                          |
| <span id="RBS_FIXEDORDER"></span><span id="rbs_fixedorder"></span><dl> <dt>**FIXEDORDER de RBS \_**</dt> </dl>                | [Versión 4.70.](common-control-versions.md) El control rebar siempre muestra bandas en el mismo orden. Puede mover bandas a distintas filas, pero el orden de banda es estático.<br/>                                                                                                                                                                      |
| <span id="RBS_REGISTERDROP"></span><span id="rbs_registerdrop"></span><dl> <dt>**RBS \_ REGISTERDROP**</dt> </dl>          | [Versión 4.71.](common-control-versions.md) El control rebar genera códigos [de notificación \_ GETOBJECT](rbn-getobject.md) de RBN cuando se arrastra un objeto sobre una banda del control. Para recibir las notificaciones GETOBJECT de RBN, inicialice OLE con una llamada \_ a [**OleInitialize**](/windows/desktop/api/ole2/nf-ole2-oleinitialize) o [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize).<br/> |
| <span id="RBS_TOOLTIPS"></span><span id="rbs_tooltips"></span><dl> <dt>**INFORMACIÓN SOBRE \_ HERRAMIENTAS DE RBS**</dt> </dl>                      | [Versión 4.71.](common-control-versions.md) Todavía no se admite.<br/>                                                                                                                                                                                                                                                                                  |
| <span id="RBS_VARHEIGHT"></span><span id="rbs_varheight"></span><dl> <dt>**RBS \_ VARHEIGHT**</dt> </dl>                   | [Versión 4.71.](common-control-versions.md) El control rebar muestra bandas con el alto mínimo requerido, cuando sea posible. Sin este estilo, el control rebar muestra todas las bandas con la misma altura, usando el alto de la banda visible más alta para determinar la altura de otras bandas.<br/>                                                   |
| <span id="RBS_VERTICALGRIPPER"></span><span id="rbs_verticalgripper"></span><dl> <dt>**RBS \_ VERTICALARIAPPER**</dt> </dl> | [Versión 4.71.](common-control-versions.md) El control de tamaño se mostrará verticalmente en lugar de horizontalmente en un control de barra vertical. Este estilo se omite para los controles rebar que no tienen el [**estilo \_ CCS VERT.**](common-control-styles.md)<br/>                                                                            |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>CommCtrl.h</dt> </dl> |



 

