---
title: Editar estilos extendidos de control (CommCtrl.h)
description: En esta sección se enumeran los estilos extendidos usados al crear controles de edición. El valor de los estilos extendidos es una combinación bit a bit de estos estilos.
ms.assetid: 44ef7cbf-6d90-4ea0-8e23-cd84aacd5506
topic_type:
- apiref
api_name:
- ES_EX_ALLOWEOL_CR
- ES_EX_ALLOWEOL_LF
- ES_EX_ALLOWEOL_ALL
- ES_EX_CONVERT_EOL_ON_PASTE
- ES_EX_ZOOMABLE
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 10/19/2018
ms.openlocfilehash: 74da183ad411db5db65fb4cb9c3f32325310023c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127246921"
---
# <a name="edit-control-extended-styles"></a>Editar estilos extendidos de control

En esta sección se enumeran los estilos extendidos usados al crear controles de edición. El valor de los estilos extendidos es una combinación bit a bit de estos estilos.




| Constante | Descripción | 
|----------|-------------|
| <span id="ES_EX_ALLOWEOL_CR"></span><span id="es_ex_alloweol_cr"></span><dl><dt><strong>ES_EX_ALLOWEOL_CR</strong></dt></dl> | [Windows Vista y versiones posteriores.](common-control-versions.md) Habilita la compatibilidad con los caracteres de fin de línea de retorno de carro (CR) para interrumpir las líneas.<br /> | 
| <span id="ES_EX_ALLOWEOL_LF"></span><span id="es_ex_alloweol_lf"></span><dl><dt><strong>ES_EX_ALLOWEOL_LF</strong></dt></dl> | [Windows Vista y versiones posteriores.](common-control-versions.md) Habilita la compatibilidad con los caracteres de fin de línea de salto de línea (LF) para interrumpir las líneas.<br /> | 
| <span id="ES_EX_ALLOWEOL_ALL"></span><span id="es_ex_alloweol_all"></span><dl><dt><strong>ES_EX_ALLOWEOL_ALL</strong></dt></dl> | [Windows Vista y versiones posteriores.](common-control-versions.md) Habilita la compatibilidad con los caracteres de fin de línea de retorno de carro (CR) y de salto de línea (LF) para interrumpir las líneas.<br /> | 
| <span id="ES_EX_CONVERT_EOL_ON_PASTE"></span><span id="es_ex_convert_eol_on_paste"></span><dl><dt><strong>ES_EX_CONVERT_EOL_ON_PASTE</strong></dt></dl> | [Windows Vista y versiones posteriores.](common-control-versions.md) Convierte los caracteres de fin de línea habilitados para este control de edición en contenido pegado para que coincidan con el carácter de fin de línea utilizado por el documento actual.<br /> | 
| <span id="ES_EX_ZOOMABLE"></span><span id="es_ex_zoomable"></span><dl><dt><strong>ES_EX_ZOOMABLE</strong></dt></dl> | [Windows Vista y versiones posteriores.](common-control-versions.md) Habilita el zoom mediante Ctrl+MouseWheel y los mensajes [**\_ EM GETZOOM**](em-getzoom.md) / [**EM \_ SETZOOM.**](em-setzoom.md)<br /> | 




## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>CommCtrl.h</dt> </dl> |



 

 





