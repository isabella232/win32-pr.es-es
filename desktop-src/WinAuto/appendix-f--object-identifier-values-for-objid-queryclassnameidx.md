---
title: Apéndice F valores de identificador de objeto para OBJID_QUERYCLASSNAMEIDX
description: Cuando OLEACC envía un mensaje de WM \_ GETOBJECT con el parámetro lParam establecido en OBJIDQUERYCLASSNAMEIDX, muchos controles comunes o de usuario estándar (COMCTL) devuelven uno de los valores siguientes.
ms.assetid: 2a54973c-7dfa-49af-8fd0-925fafa256ad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: faffd8382820aef2cd341ce54b23c9e9e7c9a59b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105695706"
---
# <a name="appendix-f-object-identifier-values-for-objid_queryclassnameidx"></a>Apéndice F: valores de identificador de objeto para OBJID \_ QUERYCLASSNAMEIDX

Cuando OLEACC envía un mensaje de [**WM \_ GETOBJECT**](wm-getobject.md) con el parámetro *lParam* establecido en OBJIDQUERYCLASSNAMEIDX, muchos controles comunes o de usuario estándar (COMCTL) devuelven uno de los valores siguientes.



| Control de usuario o común | Valor devuelto |
|------------------------|--------------|
| Listbox                | 65536 + 0      |
| Botón                 | 65536 + 2      |
| estática                 | 65536 + 3      |
| Editar                   | 65536 + 4      |
| ComboBox               | 65536 + 5      |
| Barra de desplazamiento              | 65536 + 10     |
| Status                 | 65536 + 11     |
| Barra de herramientas                | 65536 + 12     |
| Progreso               | 65536 + 13     |
| Dicha                | 65536 + 14     |
| Pestaña                    | 65536 + 15     |
| Tecla de acceso rápido                 | 65536 + 16     |
| Encabezado                 | 65536 + 17     |
| TrackBar               | 65536 + 18     |
| ListView               | 65536 + 19     |
| Cuadro numérico                 | 65536 + 22     |
| Información sobre herramientas               | 65536 + 24     |
| Vista               | 65536 + 25     |
| RichEdit               | 65536 + 28     |



 

Solo los controles comunes de usuario y de Windows (COMCTL) devolverán uno de los valores de la tabla. Si una ventana devuelve 0 en respuesta a este mensaje, la ventana puede ser una de las siguientes:

-   Un control personalizado
-   Control distinto de uno de los controles de la tabla anterior.
-   Una versión anterior de un control del sistema que no reconoce el mensaje de [**WM \_ GETOBJECT**](wm-getobject.md)

Si una ventana devuelve 0, es posible que los clientes tengan que usar [**RealGetWindowClass**](/windows/win32/api/winuser/nf-winuser-realgetwindowclassw) o [**getClassName**](/windows/win32/api/winuser/nf-winuser-getclassname). Puede utilizar estas funciones para determinar el tipo de control basado en el nombre de clase.

En general, los clientes pueden usar la información proporcionada por OLEACC.

 

 