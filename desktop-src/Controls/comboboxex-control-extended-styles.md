---
title: Estilos extendidos de control ComboBoxEx (CommCtrl. h)
description: Admite los estilos extendidos que se enumeran en esta sección, así como la mayoría de los estilos de control de cuadro combinado estándar.
ms.assetid: 4741ac5e-1c46-4fd3-9174-b4ceb479261f
topic_type:
- apiref
api_name:
- CBES_EX_CASESENSITIVE
- CBES_EX_NOEDITIMAGE
- CBES_EX_NOEDITIMAGEINDENT
- CBES_EX_NOSIZELIMIT
- CBES_EX_PATHWORDBREAKPROC
- CBES_EX_TEXTENDELLIPSIS
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71dc92264dbd1bd2f5a4b1136d9a6138e1fcffa3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653594"
---
# <a name="comboboxex-control-extended-styles"></a>Estilos extendidos del control ComboBoxEx

Admite los estilos extendidos que se enumeran en esta sección, así como la mayoría de los estilos de control de cuadro combinado estándar.



| Constante                                                                                                                                                                                           | Descripción                                                                                                                                                                                                                                                                                                                           |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CBES_EX_CASESENSITIVE"></span><span id="cbes_ex_casesensitive"></span><dl> <dt>**CBES \_ ex \_ CASESENSITIVE**</dt> </dl>             | Las búsquedas **BSTR** en la lista distinguirán mayúsculas de minúsculas. Esto incluye las búsquedas como resultado del texto que se va a escribir en el cuadro de edición y el \_ mensaje CB FindExactString con.<br/>                                                                                                                                                          |
| <span id="CBES_EX_NOEDITIMAGE"></span><span id="cbes_ex_noeditimage"></span><dl> <dt>**CBES \_ ex \_ NOEDITIMAGE**</dt> </dl>                   | En el cuadro de edición y en la lista desplegable no se mostrarán las imágenes del elemento. <br/>                                                                                                                                                                                                                                                          |
| <span id="CBES_EX_NOEDITIMAGEINDENT"></span><span id="cbes_ex_noeditimageindent"></span><dl> <dt>**CBES \_ ex \_ NOEDITIMAGEINDENT**</dt> </dl> | En el cuadro de edición y en la lista desplegable no se mostrarán las imágenes del elemento. <br/>                                                                                                                                                                                                                                                          |
| <span id="CBES_EX_NOSIZELIMIT"></span><span id="cbes_ex_nosizelimit"></span><dl> <dt>**CBES \_ ex \_ NOSIZELIMIT**</dt> </dl>                   | Permite que el control ComboBoxEx tenga un tamaño vertical menor que el control de cuadro combinado que contiene. Si el tamaño de ComboBoxEx es menor que el cuadro combinado, el cuadro combinado se recortará. <br/>                                                                                                                                  |
| <span id="CBES_EX_PATHWORDBREAKPROC"></span><span id="cbes_ex_pathwordbreakproc"></span><dl> <dt>**CBES \_ ex \_ PATHWORDBREAKPROC**</dt> </dl> | Solo Windows NT. El cuadro de edición utilizará la barra diagonal (/), la barra diagonal inversa ( \) y los caracteres de punto (.) como delimitadores de palabras. Esto hace que los métodos abreviados de teclado para el movimiento de cursor de palabra por palabra funcionen en los nombres de ruta de acceso y las direcciones URL.<br/>                                                                                                       |
| <span id="CBES_EX_TEXTENDELLIPSIS"></span><span id="cbes_ex_textendellipsis"></span><dl> <dt>**CBES \_ ex \_ TEXTENDELLIPSIS**</dt> </dl>       | **Windows Vista y versiones posteriores.** Hace que los elementos de la lista desplegable y el cuadro de edición (cuando el cuadro de edición es de solo lectura) se trunquen con puntos suspensivos ("...") en lugar de simplemente recortados por el borde del control. Esto resulta útil cuando el control debe establecerse en un ancho fijo, pero las entradas de la lista pueden ser largas.<br/> |



## <a name="remarks"></a>Observaciones

Los estilos extendidos de ComboBox se establecen y recuperan mediante los mensajes [**CBEM \_ SETEXTENDEDSTYLE**](cbem-setextendedstyle.md) y [**CBEM \_ GETEXTENDEDSTYLE**](cbem-getextendedstyle.md) .

> [!Note]  
> Si intenta establecer un estilo extendido para un control ComboBoxEx creado con el estilo [**\_ simple CBS**](combo-box-styles.md) , es posible que no se vuelva a dibujar correctamente. El **estilo \_ simple CBS** tampoco funciona correctamente con el \_ estilo extendido CBES ex \_ PATHWORDBREAKPROC.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>CommCtrl. h</dt> </dl> |



 

 





