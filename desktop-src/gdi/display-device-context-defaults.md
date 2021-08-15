---
description: Al crear primero un contexto de dispositivo para mostrar, el sistema asigna valores predeterminados para los atributos (es decir, objetos de dibujo, colores y modos) que componen el contexto del dispositivo.
ms.assetid: 1a9244e6-2773-435a-8569-806df3a0cd39
title: Mostrar valores predeterminados de contexto de dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 366c4ecb861b64d2b69836832259e6820e0f8809e4aa478d074220d133ccec55
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117887282"
---
# <a name="display-device-context-defaults"></a>Mostrar valores predeterminados de contexto de dispositivo

Al crear primero un contexto de dispositivo para mostrar, el sistema asigna valores predeterminados para los atributos (es decir, objetos de dibujo, colores y modos) que componen el contexto del dispositivo. En la tabla siguiente se muestran los valores predeterminados de los atributos de un contexto de dispositivo para mostrar.



| Atributo                             | Valor predeterminado                                                                                                                                 |
|---------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| Color de fondo                      | Configuración del color de fondo Panel de control (normalmente, blanco).                                                                               |
| Modo en segundo plano                       | Opaco                                                                                                                                        |
| Bitmap                                | Ninguno                                                                                                                                          |
| Pincel                                 | PINCEL \_ BLANCO                                                                                                                                  |
| Origen del pincel                          | (0,0)                                                                                                                                         |
| Región de recorte                       | Ventana completa o área de cliente con la región de actualización recortada, según corresponda. También se pueden recortar las ventanas secundarias y emergentes del área de cliente. |
| Paleta                               | PALETA \_ PREDETERMINADA                                                                                                                              |
| Posición actual del lápiz                  | (0,0)                                                                                                                                         |
| Origen del dispositivo                         | Esquina superior izquierda de la ventana o del área de cliente.                                                                                           |
| Modo de dibujo                          | R2 \_ COPYPEN                                                                                                                                   |
| Fuente                                  | FUENTE DEL \_ SISTEMA                                                                                                                                  |
| Espaciado entre caracteres                | 0                                                                                                                                             |
| Modo de asignación                          | MM \_ TEXT                                                                                                                                      |
| Lápiz                                   | LÁPIZ \_ NEGRO                                                                                                                                    |
| [**Modo de**](/windows/desktop/api/Wingdi/nf-wingdi-polygon) relleno de polígono | Alternativo                                                                                                                                     |
| Modo stretch                          | BLACKONWHITE                                                                                                                                  |
| Color del texto                            | Configuración de color de texto Panel de control (normalmente, negro).                                                                                     |
| Extensión de ventanilla                       | (1,1)                                                                                                                                         |
| Origen de la ventanilla                       | (0,0)                                                                                                                                         |
| Extensión de ventana                         | (1,1)                                                                                                                                         |
| Origen de la ventana                         | (0,0)                                                                                                                                         |



 

Una aplicación puede modificar los valores de los atributos de contexto del dispositivo para mostrar mediante funciones de selección y atributo, como [**SelectObject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject), [**SetMapMode**](/windows/desktop/api/Wingdi/nf-wingdi-setmapmode)y [**SetTextColor.**](/windows/desktop/api/Wingdi/nf-wingdi-settextcolor) Por ejemplo, una aplicación puede modificar las unidades de medida predeterminadas en el sistema de coordenadas mediante **SetMapMode** para cambiar el modo de asignación.

Los cambios en los valores de atributo de un contexto de dispositivo común, primario o de ventana no son permanentes. Cuando una aplicación libera estos contextos de dispositivo, las selecciones actuales, como el modo de asignación y la región de recorte, se pierden a medida que el contexto se devuelve a la memoria caché. Los cambios en un contexto de clase o dispositivo privado persisten indefinidamente. Para restaurarlos a sus valores predeterminados originales, una aplicación debe establecer explícitamente cada atributo.

 

 



