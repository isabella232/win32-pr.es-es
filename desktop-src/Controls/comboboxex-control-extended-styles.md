---
title: Estilos extendidos del control ComboBoxEx (CommCtrl.h)
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
ms.openlocfilehash: 966d259cf427bcc83e9a8b2fb65670a2a05b9458
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111387661"
---
# <a name="comboboxex-control-extended-styles"></a>Estilos extendidos del control ComboBoxEx

Admite los estilos extendidos que se enumeran en esta sección, así como la mayoría de los estilos de control de cuadro combinado estándar.



| Constante                                                                                                                                                                                           | Descripción                                                                                                                                                                                                                                                                                                                           |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CBES_EX_CASESENSITIVE"></span><span id="cbes_ex_casesensitive"></span><dl> <dt>**CBES \_ EX \_ CASESENSITIVE**</dt> </dl>             | **Las búsquedas BSTR** de la lista distinguen mayúsculas de minúsculas. Esto incluye las búsquedas como resultado de escribir texto en el cuadro de edición y el mensaje \_ FINDSTRINGEXACT de CB.<br/>                                                                                                                                                          |
| <span id="CBES_EX_NOEDITIMAGE"></span><span id="cbes_ex_noeditimage"></span><dl> <dt>**CBES \_ EX \_ NOEDITIMAGE**</dt> </dl>                   | El cuadro de edición y la lista desplegable no mostrarán imágenes de elementos. <br/>                                                                                                                                                                                                                                                          |
| <span id="CBES_EX_NOEDITIMAGEINDENT"></span><span id="cbes_ex_noeditimageindent"></span><dl> <dt>**CBES \_ EX \_ NOEDITIMAGEINDENT**</dt> </dl> | El cuadro de edición y la lista desplegable no mostrarán imágenes de elementos. <br/>                                                                                                                                                                                                                                                          |
| <span id="CBES_EX_NOSIZELIMIT"></span><span id="cbes_ex_nosizelimit"></span><dl> <dt>**CBES \_ EX \_ NOSIZELIMIT**</dt> </dl>                   | Permite que el control ComboBoxEx tenga un tamaño vertical menor que su control de cuadro combinado contenido. Si el tamaño de ComboBoxEx es menor que el cuadro combinado, se recortará el cuadro combinado. <br/>                                                                                                                                  |
| <span id="CBES_EX_PATHWORDBREAKPROC"></span><span id="cbes_ex_pathwordbreakproc"></span><dl> <dt>**CBES \_ EX \_ PATHWORDBREAKPROC**</dt> </dl> | Solo Windows NT. El cuadro de edición usará los caracteres de barra diagonal inversa (/), barra diagonal inversa ( ) y \\ punto (.) como delimitadores de palabras. Esto hace que los métodos abreviados de teclado para el movimiento del cursor palabra a palabra sean efectivos en los nombres y direcciones URL de las rutas de acceso.<br/>                                                                                                       |
| <span id="CBES_EX_TEXTENDELLIPSIS"></span><span id="cbes_ex_textendellipsis"></span><dl> <dt>**CBES \_ EX \_ TEXTENDVELOPSIS**</dt> </dl>       | **Windows Vista y versiones posteriores.** Hace que los elementos de la lista desplegable y el cuadro de edición (cuando el cuadro de edición es de solo lectura) se trunquien con puntos suspensivos ("...") en lugar de simplemente recortarse por el borde del control. Esto resulta útil cuando el control debe establecerse en un ancho fijo, pero las entradas de la lista pueden ser largas.<br/> |



## <a name="remarks"></a>Comentarios

Establezca y recupere los estilos extendidos del cuadro combinado mediante los mensajes [**CBEM \_ SETEXTENDEDSTYLE**](cbem-setextendedstyle.md) y [**CBEM \_ GETEXTENDEDSTYLE.**](cbem-getextendedstyle.md)

> [!Note]  
> Si intenta establecer un estilo extendido para un control ComboBoxEx creado con el estilo SIMPLE de [**CBS, \_**](combo-box-styles.md) es posible que no se vuelva a dibujar correctamente. El **estilo SIMPLE \_ de CBS** tampoco funciona correctamente con el estilo extendido \_ \_ PATHWORDBREAKPROC de CBES EX.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>CommCtrl.h</dt> </dl> |



 

 





