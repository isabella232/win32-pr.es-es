---
description: En esta sección se describen las marcas usadas por los métodos de la interfaz IActiveDesktop.
title: Marcas IActiveDesktop (ShlObj. h)
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "104987487"
---
# <a name="iactivedesktop-flags"></a>Marcas de IActiveDesktop

En esta sección se describen las marcas usadas por los métodos de la interfaz [**IActiveDesktop**](/windows/win32/api/shlobj_core/nn-shlobj_core-iactivedesktop) .

<dl> <dt>

<span id="AD_APPLY_ALL"></span><span id="ad_apply_all"></span>**\_aplicar \_ todo en ad**
</dt> <dd> <dl> <dt>



Agregación de los valores de * * * * ad Apply Save * * * * \_ \_ , * * * * ad \_ Apply HTMLGEN * * * * \_ y * * * * \_ ad \_ Apply Refresh * * * *.


</dt> </dl> </dd> <dt>

<span id="AD_APPLY_BUFFERED_REFRESH"></span><span id="ad_apply_buffered_refresh"></span>**\_aplicación de \_ actualización almacenada en búfer \_**
</dt> <dd> <dl> <dt>



Inicia un temporizador y agrega todas las solicitudes de actualización realizadas con esta marca durante ese intervalo de tiempo en una única actualización. Este intervalo se establece en cinco segundos. Al final del intervalo, o si se solicita una actualización durante el intervalo sin una marca * * * * AD \_ Apply \_ buffered \_ Refresh * * * *, se realiza la actualización y se detiene el temporizador. Esta marca debe combinarse con la marca * * * * AD \_ Apply Refresh * * * * \_ .


</dt> </dl> </dd> <dt>

<span id="AD_APPLY_DYNAMICREFRESH"></span><span id="ad_apply_dynamicrefresh"></span>**\_DYNAMICREFRESH de aplicación de ad \_**
</dt> <dd> <dl> <dt>



[Versión 5,0](versions.md). Use HTML dinámico para actualizar solo los elementos que han cambiado desde la última actualización, no todo el escritorio.


</dt> </dl> </dd> <dt>

<span id="AD_APPLY_FORCE"></span><span id="ad_apply_force"></span>**\_fuerza de aplicación de ad \_**
</dt> <dd> <dl> <dt>



Forzar un cambio de Active Desktop.


</dt> </dl> </dd> <dt>

<span id="AD_APPLY_HTMLGEN"></span><span id="ad_apply_htmlgen"></span>**\_HTMLGEN de aplicación de ad \_**
</dt> <dd> <dl> <dt>



Vuelva a generar el archivo HTML del escritorio.


</dt> </dl> </dd> <dt>

<span id="AD_APPLY_REFRESH"></span><span id="ad_apply_refresh"></span>**\_actualización de aplicación de ad \_**
</dt> <dd> <dl> <dt>



Actualice el elemento de escritorio.


</dt> </dl> </dd> <dt>

<span id="AD_APPLY_SAVE"></span><span id="ad_apply_save"></span>**\_aplicar \_ guardado de ad**
</dt> <dd> <dl> <dt>



Guarde el elemento de escritorio.


</dt> </dl> </dd> <dt>

<span id="COMP_ELEM_ALL"></span><span id="comp_elem_all"></span>**\_todo Elem \_ todo**
</dt> <dd> <dl> <dt>



Agregación de los valores de Elem de COMP \_ \_ \* .


</dt> </dl> </dd> <dt>

<span id="COMP_ELEM_CHECKED"></span><span id="comp_elem_checked"></span>**COMP \_ Elem \_ activada**
</dt> <dd> <dl> <dt>



El elemento se ha comprobado.


</dt> </dl> </dd> <dt>

<span id="COMP_ELEM_CURITEMSTATE"></span><span id="comp_elem_curitemstate"></span>**COMP \_ Elem \_ CURITEMSTATE**
</dt> <dd> <dl> <dt>



Estado actual del elemento de escritorio.


</dt> </dl> </dd> <dt>

<span id="COMP_ELEM_FRIENDLYNAME"></span><span id="comp_elem_friendlyname"></span>**COMP \_ Elem \_ FRIENDLYNAME**
</dt> <dd> <dl> <dt>



Nombre descriptivo del elemento.


</dt> </dl> </dd> <dt>

<span id="COMP_ELEM_NOSCROLL"></span><span id="comp_elem_noscroll"></span>**COMP \_ Elem \_ noscroll**
</dt> <dd> <dl> <dt>



El elemento no es desplazable.


</dt> </dl> </dd> <dt>

<span id="COMP_ELEM_ORIGINAL_CSI"></span><span id="comp_elem_original_csi"></span>**COMPt \_ Elem \_ original \_ CSI**
</dt> <dd> <dl> <dt>



Información de estado del elemento de escritorio original.


</dt> </dl> </dd> <dt>

<span id="COMP_ELEM_POS_LEFT"></span><span id="comp_elem_pos_left"></span>**\_OC Elem \_ pos \_ izquierda**
</dt> <dd> <dl> <dt>



Posición horizontal del elemento.


</dt> </dl> </dd> <dt>

<span id="COMP_ELEM_POS_TOP"></span><span id="comp_elem_pos_top"></span>**\_borde de Elem Elem \_ \_**
</dt> <dd> <dl> <dt>



Posición vertical del elemento.


</dt> </dl> </dd> <dt>

<span id="COMP_ELEM_POS_ZINDEX"></span><span id="comp_elem_pos_zindex"></span>**COMP \_ Elem \_ pos \_ ZINDEX**
</dt> <dd> <dl> <dt>



Índice z del elemento.


</dt> </dl> </dd> <dt>

<span id="COMP_ELEM_RESTORED_CSI"></span><span id="comp_elem_restored_csi"></span>**COMP \_ Elem \_ restaurada \_ CSI**
</dt> <dd> <dl> <dt>



Información de estado del elemento de escritorio restaurada.


</dt> </dl> </dd> <dt>

<span id="COMP_ELEM_SIZE_HEIGHT"></span><span id="comp_elem_size_height"></span>**\_altura del \_ tamaño de Elem. \_**
</dt> <dd> <dl> <dt>



Alto del elemento.


</dt> </dl> </dd> <dt>

<span id="COMP_ELEM_SIZE_WIDTH"></span><span id="comp_elem_size_width"></span>**\_ancho de \_ tamaño de Elem. \_**
</dt> <dd> <dl> <dt>



Ancho del elemento.


</dt> </dl> </dd> <dt>

<span id="COMP_ELEM_SOURCE"></span><span id="comp_elem_source"></span>**\_origen de Elem. \_**
</dt> <dd> <dl> <dt>



Origen original del elemento.


</dt> </dl> </dd> <dt>

<span id="COMP_ELEM_TYPE"></span><span id="comp_elem_type"></span>**\_tipo Elem. de comp. \_**
</dt> <dd> <dl> <dt>



Tipo de elemento.


</dt> </dl> </dd> <dt>

<span id="COMP_TYPE_CFHTML"></span><span id="comp_type_cfhtml"></span>**\_tipo COMP \_ CFHTML**
</dt> <dd> <dl> <dt>



Formato HTML comprimido.


</dt> </dl> </dd> <dt>

<span id="COMP_TYPE_CONTROL"></span><span id="comp_type_control"></span>**\_control de tipo COMP \_**
</dt> <dd> <dl> <dt>



El elemento es un control.


</dt> </dl> </dd> <dt>

<span id="COMP_TYPE_HTMLDOC"></span><span id="comp_type_htmldoc"></span>**\_tipo COMP \_ HTMLDOC**
</dt> <dd> <dl> <dt>



El elemento es un documento HTML. Esta marca solo se debe usar cuando sea absolutamente necesario. Hace que un documento HTML se inserte literalmente en el archivo Desktop. htt que se usa para controlar el diseño del escritorio. En la mayoría de los casos, debe usar la marca * * * * tipo de COMP \_ \_ website * * * * para agregar elementos al escritorio.


</dt> </dl> </dd> <dt>

<span id="COMP_TYPE_MAX"></span><span id="comp_type_max"></span>**\_tipo COMP \_ máx.**
</dt> <dd> <dl> <dt>



Valor máximo de una marca de \_ tipo COMP \_ \* .


</dt> </dl> </dd> <dt>

<span id="COMP_TYPE_PICTURE"></span><span id="comp_type_picture"></span>**\_imagen del tipo COMP \_**
</dt> <dd> <dl> <dt>



El elemento es una imagen.


</dt> </dl> </dd> <dt>

<span id="COMP_TYPE_WEBSITE"></span><span id="comp_type_website"></span>**\_sitio web de tipo COMP \_**
</dt> <dd> <dl> <dt>



El elemento es un sitio Web.


</dt> </dl> </dd> <dt>

<span id="COMPONENT_TOP"></span><span id="component_top"></span>**\_parte superior del componente**
</dt> <dd> <dl> <dt>



Un valor de orden z que significa que el elemento está en la parte superior.


</dt> </dl> </dd> <dt>

<span id="WPSTYLE_CENTER"></span><span id="wpstyle_center"></span>**Centro de WPSTYLE \_**
</dt> <dd> <dl> <dt>



El papel tapiz está centrado.


</dt> </dl> </dd> <dt>

<span id="WPSTYLE_MAX"></span><span id="wpstyle_max"></span>**WPSTYLE \_ máx.**
</dt> <dd> <dl> <dt>



Valor máximo de una marca WPSTYLE \_ \* .


</dt> </dl> </dd> <dt>

<span id="WPSTYLE_STRETCH"></span><span id="wpstyle_stretch"></span>**WPSTYLE \_ Stretch**
</dt> <dd> <dl> <dt>



El papel tapiz se ajusta para ajustarse a toda la pantalla.


</dt> </dl> </dd> <dt>

<span id="WPSTYLE_TILE"></span><span id="wpstyle_tile"></span>**icono de WPSTYLE \_**
</dt> <dd> <dl> <dt>



El papel tapiz está en mosaico.


</dt> </dl> </dd> <dt>

<span id="WPSTYLE_SPAN"></span><span id="wpstyle_span"></span>**\_intervalo WPSTYLE**
</dt> <dd> <dl> <dt>



**Windows 8 y versiones posteriores**: el papel tapiz abarca varios monitores.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>ShlObj. h</dt> </dl> |



 

 
