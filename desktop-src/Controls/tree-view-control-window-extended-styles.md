---
title: Tree-View controles extendidos (CommCtrl.h)
description: En esta sección se enumeran los estilos extendidos que se usan al crear controles de vista de árbol. El valor de los estilos extendidos es una combinación bit a bit de estos estilos.
ms.assetid: b45e7b7c-2c7b-49fa-8679-57c478b2f796
topic_type:
- apiref
api_name:
- TVS_EX_AUTOHSCROLL
- TVS_EX_DIMMEDCHECKBOXES
- TVS_EX_DOUBLEBUFFER
- TVS_EX_DRAWIMAGEASYNC
- TVS_EX_EXCLUSIONCHECKBOXES
- TVS_EX_FADEINOUTEXPANDOS
- TVS_EX_MULTISELECT
- TVS_EX_NOINDENTSTATE
- TVS_EX_NOSINGLECOLLAPSE
- TVS_EX_PARTIALCHECKBOXES
- TVS_EX_RICHTOOLTIP
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eed135e5c1cfd335333251c183b408a59d2768ac
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127165965"
---
# <a name="tree-view-control-extended-styles"></a>Tree-View controles extendidos

En esta sección se enumeran los estilos extendidos que se usan al crear controles de vista de árbol. El valor de los estilos extendidos es una combinación bit a bit de estos estilos.




| Constante | Descripción | 
|----------|-------------|
| <span id="TVS_EX_AUTOHSCROLL"></span><span id="tvs_ex_autohscroll"></span><dl><dt><strong>TVS_EX_AUTOHSCROLL</strong></dt></dl> | <a href="common-control-versions.md">Windows Vista</a>. Quite la barra de desplazamiento horizontal y el desplazamiento automático en función de la posición del mouse.<br /> | 
| <span id="TVS_EX_DIMMEDCHECKBOXES"></span><span id="tvs_ex_dimmedcheckboxes"></span><dl><dt><strong>TVS_EX_DIMMEDCHECKBOXES</strong></dt></dl> | <a href="common-control-versions.md">Windows Vista</a>. Incluya el estado de casilla atenuada si el control tiene <a href="tree-view-control-window-styles.md"><strong>el TVS_CHECKBOXES</strong></a> atenuado.<br /> | 
| <span id="TVS_EX_DOUBLEBUFFER"></span><span id="tvs_ex_doublebuffer"></span><dl><dt><strong>TVS_EX_DOUBLEBUFFER</strong></dt></dl> | <a href="common-control-versions.md">Windows Vista</a>. Especifica cómo se borra o rellena el fondo.<br /> | 
| <span id="TVS_EX_DRAWIMAGEASYNC"></span><span id="tvs_ex_drawimageasync"></span><dl><dt><strong>TVS_EX_DRAWIMAGEASYNC</strong></dt></dl> | <a href="common-control-versions.md">Windows Vista</a>. Recupera información de cuadrícula de calendario.<br /> | 
| <span id="TVS_EX_EXCLUSIONCHECKBOXES"></span><span id="tvs_ex_exclusioncheckboxes"></span><dl><dt><strong>TVS_EX_EXCLUSIONCHECKBOXES</strong></dt></dl> | <a href="common-control-versions.md">Windows Vista</a>. Incluya el estado de la casilla de exclusión si el control <a href="tree-view-control-window-styles.md"><strong>tiene el TVS_CHECKBOXES</strong></a> de exclusión.<br /> | 
| <span id="TVS_EX_FADEINOUTEXPANDOS"></span><span id="tvs_ex_fadeinoutexpandos"></span><dl><dt><strong>TVS_EX_FADEINOUTEXPANDOS</strong></dt></dl> | <a href="common-control-versions.md">Windows Vista</a>. Los botones de expansión de atenuación se desplazan hacia dentro o hacia fuera cuando el mouse se aleja o pasa al estado de mantener el puntero sobre el control.<br /> | 
| <span id="TVS_EX_MULTISELECT"></span><span id="tvs_ex_multiselect"></span><dl><dt><strong>TVS_EX_MULTISELECT</strong></dt></dl> | No compatible. No debe usarse.<br /> | 
| <span id="TVS_EX_NOINDENTSTATE"></span><span id="tvs_ex_noindentstate"></span><dl><dt><strong>TVS_EX_NOINDENTSTATE</strong></dt></dl> | <a href="common-control-versions.md">Windows Vista</a>. No aplique sangría a la vista de árbol para los botones expando.<br /> | 
| <span id="TVS_EX_NOSINGLECOLLAPSE"></span><span id="tvs_ex_nosinglecollapse"></span><dl><dt><strong>TVS_EX_NOSINGLECOLLAPSE</strong></dt></dl> | <a href="common-control-versions.md">Windows Vista</a>. <strong>Diseñado para uso interno; no se recomienda para su uso en aplicaciones.</strong> No contraiga el elemento de vista de árbol seleccionado previamente a menos que tenga el mismo elemento primario que la nueva selección. Este estilo debe usarse con el <a href="tree-view-control-window-styles.md"><strong>TVS_SINGLEEXPAND</strong></a> estilo. <br /><blockquote>[!Note]<br />Es posible que este estilo no se pueda usar en versiones futuras de Comctl32.dll. Además, este estilo no se define en commctrl.h. Agregue la siguiente definición a los archivos de origen de la aplicación para usar este estilo: <code>#define TVS_EX_NOSINGLECOLLAPSE 0x0001</code></blockquote><br /> | 
| <span id="TVS_EX_PARTIALCHECKBOXES"></span><span id="tvs_ex_partialcheckboxes"></span><dl><dt><strong>TVS_EX_PARTIALCHECKBOXES</strong></dt></dl> | <a href="common-control-versions.md">Windows Vista</a>. Incluya el estado de casilla parcial si el control tiene <a href="tree-view-control-window-styles.md"><strong>el TVS_CHECKBOXES</strong></a> de verificación.<br /> | 
| <span id="TVS_EX_RICHTOOLTIP"></span><span id="tvs_ex_richtooltip"></span><dl><dt><strong>TVS_EX_RICHTOOLTIP</strong></dt></dl> | <a href="common-control-versions.md">Windows Vista</a>. Permitir información sobre herramientas enriquecte en la vista de árbol (dibujada de forma personalizada con icono y texto).<br /> | 




## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>CommCtrl.h</dt> </dl> |



 

 





