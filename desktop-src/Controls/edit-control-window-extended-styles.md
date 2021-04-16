---
title: Estilos extendidos del control de edición (CommCtrl. h)
description: En esta sección se enumeran los estilos extendidos que se usan al crear controles de edición. El valor de los estilos extendidos es una combinación bit a bit de estos estilos.
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
ms.openlocfilehash: 912a13b0e05d7b12e5058435221b821b50eddf2e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649720"
---
# <a name="edit-control-extended-styles"></a>Estilos extendidos de control de edición

En esta sección se enumeran los estilos extendidos que se usan al crear controles de edición. El valor de los estilos extendidos es una combinación bit a bit de estos estilos.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Constante</th>
<th style="text-align: left;">Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="ES_EX_ALLOWEOL_CR"></span><span id="es_ex_alloweol_cr"></span><dl> <dt><strong>ES_EX_ALLOWEOL_CR</strong></dt> </dl></td>
<td style="text-align: left;">[Windows Vista y versiones posteriores](common-control-versions.md). Habilita la compatibilidad con los caracteres de fin de línea de retorno de carro (CR) para dividir las líneas.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="ES_EX_ALLOWEOL_LF"></span><span id="es_ex_alloweol_lf"></span><dl> <dt><strong>ES_EX_ALLOWEOL_LF</strong></dt> </dl></td>
<td style="text-align: left;">[Windows Vista y versiones posteriores](common-control-versions.md). Habilita la compatibilidad con los caracteres de fin de línea de avance de línea para romper las líneas.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="ES_EX_ALLOWEOL_ALL"></span><span id="es_ex_alloweol_all"></span><dl> <dt><strong>ES_EX_ALLOWEOL_ALL</strong></dt> </dl></td>
<td style="text-align: left;">[Windows Vista y versiones posteriores](common-control-versions.md). Habilita la compatibilidad con los caracteres de fin de línea de retorno de carro (CR) y avance de línea (LF) para dividir las líneas.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="ES_EX_CONVERT_EOL_ON_PASTE"></span><span id="es_ex_convert_eol_on_paste"></span><dl> <dt><strong>ES_EX_CONVERT_EOL_ON_PASTE</strong></dt> </dl></td>
<td style="text-align: left;">[Windows Vista y versiones posteriores](common-control-versions.md). Convierte los caracteres de fin de línea habilitados para este control de edición en el contenido pegado para que coincida con el carácter de final de línea utilizado por el documento actual.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="ES_EX_ZOOMABLE"></span><span id="es_ex_zoomable"></span><dl> <dt><strong>ES_EX_ZOOMABLE</strong></dt> </dl></td>
<td style="text-align: left;">[Windows Vista y versiones posteriores](common-control-versions.md). Habilita el zoom con Ctrl + MouseWheel y los [**mensajes \_ GETZOOM**](em-getzoom.md) / [**em \_ SETZOOM**](em-setzoom.md) .<br/></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>CommCtrl. h</dt> </dl> |



 

 





