---
title: Estilos de control rebar (CommCtrl. h)
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660538"
---
# <a name="rebar-control-styles"></a>Estilos de control rebar

Los controles rebar admiten una variedad de estilos de control además de los estilos de ventana estándar.



| Constante                                                                                                                                                                        | Descripción                                                                                                                                                                                                                                                                                                                                                 |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RBS_AUTOSIZE"></span><span id="rbs_autosize"></span><dl> <dt>**\_tamaño automático de RBS**</dt> </dl>                      | [Versión 4,71](common-control-versions.md). El control rebar cambiará automáticamente el diseño de las bandas cuando cambie el tamaño o la posición del control. Cuando esto ocurre, se enviará una notificación de [ \_ tamaño automático de RBN](rbn-autosize.md) .<br/>                                                                                              |
| <span id="RBS_BANDBORDERS"></span><span id="rbs_bandborders"></span><dl> <dt>**BANDBORDERS de RBS \_**</dt> </dl>             | [Versión 4,71](common-control-versions.md). El control rebar muestra líneas estrechas para separar las bandas adyacentes.<br/>                                                                                                                                                                                                                                 |
| <span id="RBS_DBLCLKTOGGLE"></span><span id="rbs_dblclktoggle"></span><dl> <dt>**DBLCLKTOGGLE de RBS \_**</dt> </dl>          | [Versión 4,71](common-control-versions.md). Cuando el usuario hace doble clic en la banda, la banda rebar alterna su estado maximizado o minimizado. Sin este estilo, el estado maximizado o minimizado se alterna cuando el usuario hace clic en la banda.<br/>                                                                                          |
| <span id="RBS_FIXEDORDER"></span><span id="rbs_fixedorder"></span><dl> <dt>**FIXEDORDER de RBS \_**</dt> </dl>                | [Versión 4,70](common-control-versions.md). El control rebar siempre muestra las bandas en el mismo orden. Puede trasladar bandas a filas diferentes, pero el orden de las bandas es estático.<br/>                                                                                                                                                                      |
| <span id="RBS_REGISTERDROP"></span><span id="rbs_registerdrop"></span><dl> <dt>**REGISTERDROP de RBS \_**</dt> </dl>          | [Versión 4,71](common-control-versions.md). El control rebar genera códigos de notificación [RBN \_ GETOBJECT](rbn-getobject.md) cuando se arrastra un objeto sobre una banda en el control. Para recibir \_ notificaciones GETOBJECT de RBN, INICIALICE OLE con una llamada a [**OleInitialize**](/windows/desktop/api/ole2/nf-ole2-oleinitialize) o [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize).<br/> |
| <span id="RBS_TOOLTIPS"></span><span id="rbs_tooltips"></span><dl> <dt>**\_información sobre herramientas de RBS**</dt> </dl>                      | [Versión 4,71](common-control-versions.md). Todavía no se admite.<br/>                                                                                                                                                                                                                                                                                  |
| <span id="RBS_VARHEIGHT"></span><span id="rbs_varheight"></span><dl> <dt>**VARHEIGHT de RBS \_**</dt> </dl>                   | [Versión 4,71](common-control-versions.md). El control rebar muestra las bandas con el alto mínimo necesario, siempre que sea posible. Sin este estilo, el control rebar muestra todas las bandas con el mismo alto, utilizando el alto de la banda visible más alta para determinar el alto de otras bandas.<br/>                                                   |
| <span id="RBS_VERTICALGRIPPER"></span><span id="rbs_verticalgripper"></span><dl> <dt>**VERTICALGRIPPER de RBS \_**</dt> </dl> | [Versión 4,71](common-control-versions.md). El control de tamaño se mostrará verticalmente en lugar de horizontalmente en un control rebar vertical. Este estilo se omite para los controles Rebar que no tienen el estilo [**CCS \_ Vert**](common-control-styles.md) .<br/>                                                                            |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>CommCtrl. h</dt> </dl> |



 

