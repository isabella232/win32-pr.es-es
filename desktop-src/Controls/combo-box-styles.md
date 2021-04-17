---
title: Estilos de cuadro combinado (CommCtrl. h)
description: Para crear un cuadro combinado mediante la función CreateWindow o CreateWindowEx, especifique la clase COMBOBOX, las constantes de estilo de ventana apropiadas y una combinación de los siguientes estilos de cuadro combinado.
ms.assetid: 4dc347b2-7da7-4aa0-b61f-781acf652d84
topic_type:
- apiref
api_name:
- CBS_AUTOHSCROLL
- CBS_DISABLENOSCROLL
- CBS_DROPDOWN
- CBS_DROPDOWNLIST
- CBS_HASSTRINGS
- CBS_LOWERCASE
- CBS_NOINTEGRALHEIGHT
- CBS_OEMCONVERT
- CBS_OWNERDRAWFIXED
- CBS_OWNERDRAWVARIABLE
- CBS_SIMPLE
- CBS_SORT
- CBS_UPPERCASE
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74f531b93725f3aa92778a42bae3dd3fd972534e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653595"
---
# <a name="combo-box-styles"></a>Estilos de cuadro combinado

Para crear un cuadro combinado mediante la función [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) o [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) , especifique la clase ComboBox, las constantes de estilo de ventana apropiadas y una combinación de los siguientes estilos de cuadro combinado.



| Constante                                                                                                                                                                              | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CBS_AUTOHSCROLL"></span><span id="cbs_autohscroll"></span><dl> <dt>**CBS \_ AUTOHSCROLL**</dt> </dl>                   | Desplaza automáticamente el texto en un control de edición hacia la derecha cuando el usuario escribe un carácter al final de la línea. Si no se establece este estilo, solo se permite el texto que entre dentro del límite rectangular.<br/>                                                                                                                                                                                                                                                                                  |
| <span id="CBS_DISABLENOSCROLL"></span><span id="cbs_disablenoscroll"></span><dl> <dt>**CBS \_ DISABLENOSCROLL**</dt> </dl>       | Muestra una barra de desplazamiento vertical deshabilitada en el cuadro de lista cuando el cuadro no contiene suficientes elementos para desplazarse. Sin este estilo, la barra de desplazamiento está oculta cuando el cuadro de lista no contiene suficientes elementos.<br/>                                                                                                                                                                                                                                                                                          |
| <span id="CBS_DROPDOWN"></span><span id="cbs_dropdown"></span><dl> <dt>**\_lista desplegable de CBS**</dt> </dl>                            | Similar a CBS \_ simple, con la excepción de que el cuadro de lista no se muestra a menos que el usuario seleccione un icono junto al control de edición.<br/>                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="CBS_DROPDOWNLIST"></span><span id="cbs_dropdownlist"></span><dl> <dt>**DROPDOWNLIST de CBS \_**</dt> </dl>                | Similar a \_ la lista desplegable de CBS, salvo que el control de edición se reemplaza por un elemento de texto estático que muestra la selección actual en el cuadro de lista.<br/>                                                                                                                                                                                                                                                                                                                                                     |
| <span id="CBS_HASSTRINGS"></span><span id="cbs_hasstrings"></span><dl> <dt>**CBS \_ HASSTRINGS**</dt> </dl>                      | Especifica que un cuadro combinado dibujado por el propietario contiene elementos que se componen de cadenas. El cuadro combinado mantiene la memoria y la dirección de las cadenas, por lo que la aplicación puede utilizar el mensaje [**CB \_ GETLBTEXT**](cb-getlbtext.md) para recuperar el texto de un elemento determinado.<br/> Para problemas de accesibilidad, vea [exponer Owner-Drawn elementos del cuadro combinado](/windows/desktop/WinAuto/exposing-owner-drawn-combo-box-items) .<br/>                                                                                               |
| <span id="CBS_LOWERCASE"></span><span id="cbs_lowercase"></span><dl> <dt>**CBS en \_ minúsculas**</dt> </dl>                         | Convierte en minúsculas todo el texto en el campo de selección y en la lista. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="CBS_NOINTEGRALHEIGHT"></span><span id="cbs_nointegralheight"></span><dl> <dt>**CBS \_ NOINTEGRALHEIGHT**</dt> </dl>    | Especifica que el tamaño del cuadro combinado es exactamente el tamaño especificado por la aplicación cuando creó el cuadro combinado. Normalmente, el sistema ajusta el tamaño de un cuadro combinado para que no muestre elementos parciales.<br/>                                                                                                                                                                                                                                                                                        |
| <span id="CBS_OEMCONVERT"></span><span id="cbs_oemconvert"></span><dl> <dt>**CBS \_ OEMCONVERT**</dt> </dl>                      | Convierte el texto especificado en el control de edición del cuadro combinado del juego de caracteres de Windows al Juego de caracteres OEM y, a continuación, de nuevo al Juego de caracteres de Windows. Esto garantiza una conversión de caracteres adecuada cuando la aplicación llama a la función [**CharToOem**](/windows/desktop/api/winuser/nf-winuser-chartooema) para convertir una cadena de Windows del cuadro combinado en caracteres OEM. Este estilo es muy útil para los cuadros combinados que contienen nombres de archivo y se aplica solo a los cuadros combinados creados con el \_ \_ estilo de lista desplegable CBS simple o CBS.<br/> |
| <span id="CBS_OWNERDRAWFIXED"></span><span id="cbs_ownerdrawfixed"></span><dl> <dt>**CBS \_ OWNERDRAWFIXED**</dt> </dl>          | Especifica que el propietario del cuadro de lista es responsable de dibujar su contenido y de que los elementos del cuadro de lista tienen el mismo alto. La ventana propietaria recibe un mensaje de [**\_ MEASUREITEM de WM**](wm-measureitem.md) cuando se crea el cuadro combinado y un mensaje de Windows de [**WM \_**](wm-drawitem.md) cuando cambia el aspecto visual del cuadro combinado.<br/>                                                                                                                                     |
| <span id="CBS_OWNERDRAWVARIABLE"></span><span id="cbs_ownerdrawvariable"></span><dl> <dt>**CBS \_ OWNERDRAWVARIABLE**</dt> </dl> | Especifica que el propietario del cuadro de lista es responsable de dibujar su contenido y de que los elementos del cuadro de lista tienen una altura variable. La ventana propietaria recibe un mensaje de [**\_ MEASUREITEM de WM**](wm-measureitem.md) para cada elemento del cuadro combinado cuando se crea el cuadro combinado y un mensaje de Windows de [**WM \_**](wm-drawitem.md) cuando ha cambiado un aspecto visual del cuadro combinado.<br/>                                                                                                       |
| <span id="CBS_SIMPLE"></span><span id="cbs_simple"></span><dl> <dt>**CBS \_ simple**</dt> </dl>                                  | Muestra el cuadro de lista en todo momento. La selección actual del cuadro de lista se muestra en el control de edición.<br/>                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="CBS_SORT"></span><span id="cbs_sort"></span><dl> <dt>**orden de CBS \_**</dt> </dl>                                        | Ordena automáticamente las cadenas agregadas al cuadro de lista.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| <span id="CBS_UPPERCASE"></span><span id="cbs_uppercase"></span><dl> <dt>**CBS en \_ mayúsculas**</dt> </dl>                         | Convierte a mayúsculas todo el texto en el campo de selección y en la lista.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                          |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>CommCtrl. h</dt> </dl> |



 

