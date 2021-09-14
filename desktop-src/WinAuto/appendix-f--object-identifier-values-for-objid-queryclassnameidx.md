---
title: Apéndice F Valores de identificador de objeto para OBJID_QUERYCLASSNAMEIDX
description: Cuando OLEACC envía un mensaje GETOBJECT de WM con el parámetro lParam establecido en OBJIDQUERYCLASSNAMEIDX, muchos controles USER o comunes estándar (COMCTL) devuelven uno de los \_ valores siguientes.
ms.assetid: 2a54973c-7dfa-49af-8fd0-925fafa256ad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: faffd8382820aef2cd341ce54b23c9e9e7c9a59b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127070711"
---
# <a name="appendix-f-object-identifier-values-for-objid_queryclassnameidx"></a>Apéndice F: Valores de identificador de objeto para OBJID \_ QUERYCLASSNAMEIDX

Cuando OLEACC envía un mensaje [**\_ GETOBJECT**](wm-getobject.md) de WM con el parámetro *lParam* establecido en OBJIDQUERYCLASSNAMEIDX, muchos controles USER o comunes estándar (COMCTL) devuelven uno de los valores siguientes.



| USUARIO o control común | Valor devuelto |
|------------------------|--------------|
| Listbox                | 65536+0      |
| Botón                 | 65536+2      |
| estática                 | 65536+3      |
| Editar                   | 65536+4      |
| ComboBox               | 65536+5      |
| Barra de desplazamiento              | 65536+10     |
| Status                 | 65536+11     |
| Barra de herramientas                | 65536+12     |
| Progreso               | 65536+13     |
| Animar                | 65536+14     |
| Pestaña                    | 65536+15     |
| Tecla de acceso rápido                 | 65536+16     |
| Encabezado                 | 65536+17     |
| Barra de seguimiento               | 65536+18     |
| Listview               | 65536+19     |
| Updown                 | 65536+22     |
| Tooltips               | 65536+24     |
| Treeview               | 65536+25     |
| RichEdit               | 65536+28     |



 

Solo USER Windows controles comunes (COMCTL) devolverán uno de los valores de la tabla. Si una ventana devuelve 0 en respuesta a este mensaje, la ventana puede ser una de las siguientes:

-   Un control personalizado
-   Un control distinto de uno de los controles de la tabla anterior
-   Una versión anterior de un control del sistema que no reconoce el [**mensaje \_ GETOBJECT de WM**](wm-getobject.md)

Si una ventana devuelve 0, es posible que los clientes necesiten [**usar RealGetWindowClass**](/windows/win32/api/winuser/nf-winuser-realgetwindowclassw) o [**GetClassName**](/windows/win32/api/winuser/nf-winuser-getclassname). Puede usar estas funciones para determinar el tipo de control en función del nombre de clase.

En general, los clientes pueden usar la información proporcionada por OLEACC.

 

 