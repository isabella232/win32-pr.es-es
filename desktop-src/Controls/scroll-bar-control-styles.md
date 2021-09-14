---
title: Estilos de control de barra de desplazamiento (Winuser.h)
description: Para crear un control de barra de desplazamiento mediante las funciones CreateWindow o CreateWindowEx, especifique la clase SCROLLBAR, las constantes de estilo de ventana adecuadas y una combinación de los siguientes estilos de control de barra de desplazamiento.
ms.assetid: 07195a95-eff8-4a47-926a-9d503fa7b299
topic_type:
- apiref
api_name:
- SBS_BOTTOMALIGN
- SBS_HORZ
- SBS_LEFTALIGN
- SBS_RIGHTALIGN
- SBS_SIZEBOX
- SBS_SIZEBOXBOTTOMRIGHTALIGN
- SBS_SIZEBOXTOPLEFTALIGN
- SBS_SIZEGRIP
- SBS_TOPALIGN
- SBS_VERT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7cc5de721fd4cc44867fca0dbe1b35dcaf58c6dd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127167045"
---
# <a name="scroll-bar-control-styles"></a>Estilos de control de barra de desplazamiento

Para crear un control de barra de desplazamiento mediante las funciones [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) o [**CreateWindowEx,**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) especifique la clase SCROLLBAR, las constantes de estilo de ventana adecuadas y una combinación de los siguientes estilos de control de barra de desplazamiento. Algunos de los estilos crean un control de barra de desplazamiento que usa un ancho o alto predeterminados. Sin embargo, siempre debe especificar las coordenadas X e Y y las demás dimensiones de la barra de desplazamiento al llamar a **CreateWindow** o **CreateWindowEx.**



| Constante                                                                                                                                                                                                | Descripción                                                                                                                                                                                                                                                                                                                                |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SBS_BOTTOMALIGN"></span><span id="sbs_bottomalign"></span><dl> <dt>**SBS \_ BOTTOMALIGN**</dt> </dl>                                     | Alinea el borde inferior de la barra de desplazamiento con el borde inferior del rectángulo definido por los parámetros *x*, *y*, *nWidth* y *nHeight* de la [**función CreateWindowEx.**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) La barra de desplazamiento tiene el alto predeterminado para las barras de desplazamiento del sistema. Use este estilo con el estilo \_ SBS HORZ.<br/>                      |
| <span id="SBS_HORZ"></span><span id="sbs_horz"></span><dl> <dt>**SBS \_ HORZ**</dt> </dl>                                                          | Designa una barra de desplazamiento horizontal. Si no se especifica el estilo SBS BOTTOMALIGN ni SBS TOPALIGN, la barra de desplazamiento tiene el alto, ancho y posición especificados por los parámetros \_ \_ *x*, *y*, *nWidth* y *nHeight* de [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa).<br/>                                                      |
| <span id="SBS_LEFTALIGN"></span><span id="sbs_leftalign"></span><dl> <dt>**SBS \_ LEFTALIGN**</dt> </dl>                                           | Alinea el borde izquierdo de la barra de desplazamiento con el borde izquierdo del rectángulo definido por los parámetros *x*, *y*, *nWidth* y *nHeight* de [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa). La barra de desplazamiento tiene el ancho predeterminado para las barras de desplazamiento del sistema. Use este estilo con el estilo \_ SBS VERT.<br/>                                    |
| <span id="SBS_RIGHTALIGN"></span><span id="sbs_rightalign"></span><dl> <dt>**SBS \_ RIGHTALIGN**</dt> </dl>                                        | Alinea el borde derecho de la barra de desplazamiento con el borde derecho del rectángulo definido por los parámetros *x*, *y*, *nWidth* y *nHeight* de [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa). La barra de desplazamiento tiene el ancho predeterminado para las barras de desplazamiento del sistema. Use este estilo con el estilo \_ SBS VERT.<br/>                                  |
| <span id="SBS_SIZEBOX"></span><span id="sbs_sizebox"></span><dl> <dt>**SBS \_ SIZEBOX**</dt> </dl>                                                 | Designa un cuadro de tamaño. Si no especifica el estilo SBS \_ SIZEBOXBOTTOMTOMRIGHTALIGN ni SBS \_ SIZEBOXTOPLEFTALIGN, el cuadro de tamaño tiene el alto, ancho y posición especificados por los parámetros x , y , *nWidth* y *nHeight* de [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa). <br/>                                          |
| <span id="SBS_SIZEBOXBOTTOMRIGHTALIGN"></span><span id="sbs_sizeboxbottomrightalign"></span><dl> <dt>**SBS \_ SIZEBOXBOTTOMRIGHTALIGN**</dt> </dl> | Alinea la esquina inferior derecha del cuadro de tamaño con la esquina inferior derecha del rectángulo especificado por los parámetros *x*, *y*, *nWidth* y *nHeight* de [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa). El cuadro tamaño tiene el tamaño predeterminado para los cuadros de tamaño del sistema. Use este estilo con los estilos \_ SIZEBOX o \_ SBS SIZE YAP.<br/> |
| <span id="SBS_SIZEBOXTOPLEFTALIGN"></span><span id="sbs_sizeboxtopleftalign"></span><dl> <dt>**SBS \_ SIZEBOXTOPLEFTALIGN**</dt> </dl>             | Alinea la esquina superior izquierda del cuadro de tamaño con la esquina superior izquierda del rectángulo especificado por los parámetros *x*, *y*, *nWidth* y *nHeight* de [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa). El cuadro tamaño tiene el tamaño predeterminado para los cuadros de tamaño del sistema. Use este estilo con los estilos \_ SIZEBOX o \_ SBS SIZE YAP.<br/>   |
| <span id="SBS_SIZEGRIP"></span><span id="sbs_sizegrip"></span><dl> <dt>**SBS \_ SIZEGRAP**</dt> </dl>                                              | Igual que SBS \_ SIZEBOX, pero con un borde elevado. <br/>                                                                                                                                                                                                                                                                                  |
| <span id="SBS_TOPALIGN"></span><span id="sbs_topalign"></span><dl> <dt>**SBS \_ TOPALIGN**</dt> </dl>                                              | Alinea el borde superior de la barra de desplazamiento con el borde superior del rectángulo definido por los parámetros *x*, *y*, *nWidth* y *nHeight* de [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa). La barra de desplazamiento tiene el alto predeterminado para las barras de desplazamiento del sistema. Use este estilo con el estilo \_ SBS HORZ.<br/>                                     |
| <span id="SBS_VERT"></span><span id="sbs_vert"></span><dl> <dt>**SBS \_ VERT**</dt> </dl>                                                          | Designa una barra de desplazamiento vertical. Si no especifica el estilo SBS RIGHTALIGN ni el estilo SBS LEFTALIGN, la barra de desplazamiento tiene el alto, el ancho y la posición especificados por los parámetros \_ \_ *x*, *y*, *nWidth* y *nHeight* de [**CreateWindowEx.**](/windows/desktop/api/winuser/nf-winuser-createwindowexa)<br/>                                                     |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|--------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Winuser.h</dt> </dl> |



 

