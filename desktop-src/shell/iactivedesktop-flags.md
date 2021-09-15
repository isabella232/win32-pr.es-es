---
description: En esta sección se describen las marcas usadas por los métodos de interfaz IActiveDesktop.
title: Marcas de IActiveDesktop (Shlobj.h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 6d1a2f69-0730-4805-8b50-071332ff7070
api_name:
- AD_APPLY_ALL
- AD_APPLY_BUFFERED_REFRESH
- AD_APPLY_DYNAMICREFRESH
- AD_APPLY_FORCE
- AD_APPLY_HTMLGEN
- AD_APPLY_REFRESH
- AD_APPLY_SAVE
- COMP_ELEM_ALL
- COMP_ELEM_CHECKED
- COMP_ELEM_CURITEMSTATE
- COMP_ELEM_FRIENDLYNAME
- COMP_ELEM_NOSCROLL
- COMP_ELEM_ORIGINAL_CSI
- COMP_ELEM_POS_LEFT
- COMP_ELEM_POS_TOP
- COMP_ELEM_POS_ZINDEX
- COMP_ELEM_RESTORED_CSI
- COMP_ELEM_SIZE_HEIGHT
- COMP_ELEM_SIZE_WIDTH
- COMP_ELEM_SOURCE
- COMP_ELEM_TYPE
- COMP_TYPE_CFHTML
- COMP_TYPE_CONTROL
- COMP_TYPE_HTMLDOC
- COMP_TYPE_MAX
- COMP_TYPE_PICTURE
- COMP_TYPE_WEBSITE
- COMPONENT_TOP
- WPSTYLE_CENTER
- WPSTYLE_MAX
- WPSTYLE_STRETCH
- WPSTYLE_TILE
- WPSTYLE_SPAN
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: dae164c696ae54963f802a6ddd5cb1f6862b2f14
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127468187"
---
# <a name="iactivedesktop-flags"></a>Marcas de IActiveDesktop

En esta sección se describen las marcas usadas por los métodos [**de interfaz IActiveDesktop.**](/windows/win32/api/shlobj_core/nn-shlobj_core-iactivedesktop)

<dl> <dt>

<span id="AD_APPLY_ALL"></span><span id="ad_apply_all"></span>**AD \_ APPLY \_ ALL**
</dt> <dd> <dl> <dt>



Agregado de los valores *"AD \_ \_ APPLY SAVE*", *"AD \_ APPLY \_ HTMLGEN*" y "*AD \_ APPLY \_ REFRESH*".


</dt> </dl> </dd> <dt>

<span id="AD_APPLY_BUFFERED_REFRESH"></span><span id="ad_apply_buffered_refresh"></span>**AD \_ APPLY \_ BUFFERED \_ REFRESH**
</dt> <dd> <dl> <dt>



Inicia un temporizador y agrega todas las solicitudes de actualización realizadas con esta marca durante ese intervalo de tiempo en una sola actualización. Este intervalo se establece en cinco segundos. Al final del intervalo, o si se solicita una actualización durante el intervalo sin una marca *:AD \_ APPLY \_ BUFFERED REFRESH*", se realiza la actualización y se detiene el \_ temporizador. Esta marca debe combinarse con la marca *:AD \_ APPLY \_ REFRESH*".


</dt> </dl> </dd> <dt>

<span id="AD_APPLY_DYNAMICREFRESH"></span><span id="ad_apply_dynamicrefresh"></span>**AD \_ APPLY \_ DYNAMICREFRESH**
</dt> <dd> <dl> <dt>



[Versión 5.0.](versions.md) Use HTML dinámico para actualizar solo los elementos que han cambiado desde la última actualización, no todo el escritorio.


</dt> </dl> </dd> <dt>

<span id="AD_APPLY_FORCE"></span><span id="ad_apply_force"></span>**AD \_ APPLY \_ FORCE**
</dt> <dd> <dl> <dt>



Forzar un Active Desktop cambio.


</dt> </dl> </dd> <dt>

<span id="AD_APPLY_HTMLGEN"></span><span id="ad_apply_htmlgen"></span>**AD \_ APPLY \_ HTMLGEN**
</dt> <dd> <dl> <dt>



Vuelva a generar el archivo HTML de escritorio.


</dt> </dl> </dd> <dt>

<span id="AD_APPLY_REFRESH"></span><span id="ad_apply_refresh"></span>**AD \_ APPLY \_ REFRESH**
</dt> <dd> <dl> <dt>



Actualice el elemento de escritorio.


</dt> </dl> </dd> <dt>

<span id="AD_APPLY_SAVE"></span><span id="ad_apply_save"></span>**AD \_ APPLY \_ SAVE**
</dt> <dd> <dl> <dt>



Guarde el elemento de escritorio.


</dt> </dl> </dd> <dt>

<span id="COMP_ELEM_ALL"></span><span id="comp_elem_all"></span>**COMP \_ ELEM \_ ALL**
</dt> <dd> <dl> <dt>



Agregado de los valores de COMP \_ \_ \* ELEM.


</dt> </dl> </dd> <dt>

<span id="COMP_ELEM_CHECKED"></span><span id="comp_elem_checked"></span>**COMP \_ ELEM \_ CHECKED**
</dt> <dd> <dl> <dt>



Se ha comprobado el elemento.


</dt> </dl> </dd> <dt>

<span id="COMP_ELEM_CURITEMSTATE"></span><span id="comp_elem_curitemstate"></span>**COMP \_ ELEM \_ CURITEMSTATE**
</dt> <dd> <dl> <dt>



Estado actual del elemento de escritorio.


</dt> </dl> </dd> <dt>

<span id="COMP_ELEM_FRIENDLYNAME"></span><span id="comp_elem_friendlyname"></span>**COMP \_ ELEM \_ FRIENDLYNAME**
</dt> <dd> <dl> <dt>



Nombre descriptivo del elemento.


</dt> </dl> </dd> <dt>

<span id="COMP_ELEM_NOSCROLL"></span><span id="comp_elem_noscroll"></span>**COMP \_ ELEM \_ NOSCROLL**
</dt> <dd> <dl> <dt>



El elemento no se puede desplazar.


</dt> </dl> </dd> <dt>

<span id="COMP_ELEM_ORIGINAL_CSI"></span><span id="comp_elem_original_csi"></span>**COMP \_ ELEM \_ ORIGINAL \_ CSI**
</dt> <dd> <dl> <dt>



Información de estado del elemento de escritorio original.


</dt> </dl> </dd> <dt>

<span id="COMP_ELEM_POS_LEFT"></span><span id="comp_elem_pos_left"></span>**COMP \_ ELEM \_ POS \_ LEFT**
</dt> <dd> <dl> <dt>



Posición horizontal del elemento.


</dt> </dl> </dd> <dt>

<span id="COMP_ELEM_POS_TOP"></span><span id="comp_elem_pos_top"></span>**COMP \_ ELEM \_ POS \_ TOP**
</dt> <dd> <dl> <dt>



Posición vertical del elemento.


</dt> </dl> </dd> <dt>

<span id="COMP_ELEM_POS_ZINDEX"></span><span id="comp_elem_pos_zindex"></span>**COMP \_ ELEM \_ POS \_ ZINDEX**
</dt> <dd> <dl> <dt>



Índice z del elemento.


</dt> </dl> </dd> <dt>

<span id="COMP_ELEM_RESTORED_CSI"></span><span id="comp_elem_restored_csi"></span>**COMP \_ ELEM \_ RESTORED \_ CSI**
</dt> <dd> <dl> <dt>



Información de estado del elemento de escritorio restaurado.


</dt> </dl> </dd> <dt>

<span id="COMP_ELEM_SIZE_HEIGHT"></span><span id="comp_elem_size_height"></span>**COMP \_ ELEM \_ SIZE \_ HEIGHT**
</dt> <dd> <dl> <dt>



Alto del elemento.


</dt> </dl> </dd> <dt>

<span id="COMP_ELEM_SIZE_WIDTH"></span><span id="comp_elem_size_width"></span>**COMP \_ ELEM \_ SIZE \_ WIDTH**
</dt> <dd> <dl> <dt>



Ancho del elemento.


</dt> </dl> </dd> <dt>

<span id="COMP_ELEM_SOURCE"></span><span id="comp_elem_source"></span>**COMP \_ ELEM \_ SOURCE**
</dt> <dd> <dl> <dt>



Origen original del elemento.


</dt> </dl> </dd> <dt>

<span id="COMP_ELEM_TYPE"></span><span id="comp_elem_type"></span>**COMP \_ ELEM \_ TYPE**
</dt> <dd> <dl> <dt>



Tipo de elemento.


</dt> </dl> </dd> <dt>

<span id="COMP_TYPE_CFHTML"></span><span id="comp_type_cfhtml"></span>**COMP \_ TYPE \_ CFHTML**
</dt> <dd> <dl> <dt>



Formato HTML comprimido.


</dt> </dl> </dd> <dt>

<span id="COMP_TYPE_CONTROL"></span><span id="comp_type_control"></span>**COMP \_ TYPE \_ CONTROL**
</dt> <dd> <dl> <dt>



El elemento es un control .


</dt> </dl> </dd> <dt>

<span id="COMP_TYPE_HTMLDOC"></span><span id="comp_type_htmldoc"></span>**HTMLDOC \_ DE \_ TIPO COMP**
</dt> <dd> <dl> <dt>



El elemento es un documento HTML. Esta marca solo se debe usar cuando sea absolutamente necesario. Hace que un documento HTML se inserte textualmente en el archivo Desktop.htt que se usa para controlar el diseño del escritorio. En la mayoría de los casos, debe usar la marca *"COMP \_ TYPE WEBSITE*" para agregar elementos al \_ escritorio.


</dt> </dl> </dd> <dt>

<span id="COMP_TYPE_MAX"></span><span id="comp_type_max"></span>**COMP \_ TYPE \_ MAX**
</dt> <dd> <dl> <dt>



Valor máximo de una marca COMP \_ \_ \* TYPE.


</dt> </dl> </dd> <dt>

<span id="COMP_TYPE_PICTURE"></span><span id="comp_type_picture"></span>**COMP \_ TYPE \_ PICTURE**
</dt> <dd> <dl> <dt>



El elemento es una imagen.


</dt> </dl> </dd> <dt>

<span id="COMP_TYPE_WEBSITE"></span><span id="comp_type_website"></span>**SITIO WEB \_ DE TIPO \_ COMP**
</dt> <dd> <dl> <dt>



El elemento es un sitio web.


</dt> </dl> </dd> <dt>

<span id="COMPONENT_TOP"></span><span id="component_top"></span>**COMPONENT \_ TOP**
</dt> <dd> <dl> <dt>



Valor de orden Z que significa que el elemento está en la parte superior.


</dt> </dl> </dd> <dt>

<span id="WPSTYLE_CENTER"></span><span id="wpstyle_center"></span>**WPSTYLE \_ CENTER**
</dt> <dd> <dl> <dt>



El papel tapiz está centrado.


</dt> </dl> </dd> <dt>

<span id="WPSTYLE_MAX"></span><span id="wpstyle_max"></span>**WPSTYLE \_ MAX**
</dt> <dd> <dl> <dt>



Valor máximo de una marca \_ \* WPSTYLE.


</dt> </dl> </dd> <dt>

<span id="WPSTYLE_STRETCH"></span><span id="wpstyle_stretch"></span>**WPSTYLE \_ STRETCH**
</dt> <dd> <dl> <dt>



El papel tapiz se ajusta para ajustarse a toda la pantalla.


</dt> </dl> </dd> <dt>

<span id="WPSTYLE_TILE"></span><span id="wpstyle_tile"></span>**ICONO DE \_ WPSTYLE**
</dt> <dd> <dl> <dt>



El papel tapiz está en mosaico.


</dt> </dl> </dd> <dt>

<span id="WPSTYLE_SPAN"></span><span id="wpstyle_span"></span>**INTERVALO \_ DE WPSTYLE**
</dt> <dd> <dl> <dt>



**Windows 8 y posteriores:** el papel tapiz abarca varios monitores.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Shlobj.h</dt> </dl> |



 

 
