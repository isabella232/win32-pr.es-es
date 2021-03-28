---
description: Una vez que se crea un contexto de dispositivo de pantalla, el sistema asigna los valores predeterminados de los atributos (es decir, objetos de dibujo, colores y modos) que componen el contexto del dispositivo.
ms.assetid: 1a9244e6-2773-435a-8569-806df3a0cd39
title: Mostrar valores predeterminados de contexto de dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8abcf79339d4f1cc158253d46cc3eb02ec41311
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908495"
---
# <a name="display-device-context-defaults"></a>Mostrar valores predeterminados de contexto de dispositivo

Una vez que se crea un contexto de dispositivo de pantalla, el sistema asigna los valores predeterminados de los atributos (es decir, objetos de dibujo, colores y modos) que componen el contexto del dispositivo. En la tabla siguiente se muestran los valores predeterminados de los atributos de un contexto de dispositivo de pantalla.



| Atributo                             | Valor predeterminado                                                                                                                                 |
|---------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| Color de fondo                      | Valor de color de fondo del panel de control (normalmente, blanco).                                                                               |
| Modo en segundo plano                       | OPACO                                                                                                                                        |
| Bitmap                                | Ninguno                                                                                                                                          |
| Pincel                                 | \_pincel blanco                                                                                                                                  |
| Origen del pincel                          | (0,0)                                                                                                                                         |
| Región de recorte                       | Toda la ventana o área cliente con la región de actualización recortada, según corresponda. También se pueden recortar las ventanas secundarias y las ventanas emergentes en el área de cliente. |
| Paleta                               | \_paleta predeterminada                                                                                                                              |
| Posición del lápiz actual                  | (0,0)                                                                                                                                         |
| Origen del dispositivo                         | Esquina superior izquierda de la ventana o del área cliente.                                                                                           |
| Modo de dibujo                          | \_COPYPEN R2                                                                                                                                   |
| Fuente                                  | fuente del sistema \_                                                                                                                                  |
| Espaciado entre caracteres                | 0                                                                                                                                             |
| Modo de asignación                          | \_texto mm                                                                                                                                      |
| Lápiz                                   | \_lápiz negro                                                                                                                                    |
| Modo de relleno [**poligonal**](/windows/desktop/api/Wingdi/nf-wingdi-polygon) | ALTERNATIVOS                                                                                                                                     |
| Modo de stretch                          | BLACKONWHITE                                                                                                                                  |
| Color del texto                            | Valor de color del texto del panel de control (normalmente, negro).                                                                                     |
| Extensión de la ventanilla                       | (1,1)                                                                                                                                         |
| Origen de la ventanilla                       | (0,0)                                                                                                                                         |
| Extensión de ventana                         | (1,1)                                                                                                                                         |
| Origen de la ventana                         | (0,0)                                                                                                                                         |



 

Una aplicación puede modificar los valores de los atributos de contexto de dispositivo de pantalla mediante las funciones de selección y de atributo, como [**SelectObject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject), [**SetMapMode**](/windows/desktop/api/Wingdi/nf-wingdi-setmapmode)y [**SetTextColor**](/windows/desktop/api/Wingdi/nf-wingdi-settextcolor). Por ejemplo, una aplicación puede modificar las unidades de medida predeterminadas en el sistema de coordenadas mediante **SetMapMode** para cambiar el modo de asignación.

Los cambios en los valores de atributo de un contexto de dispositivo común, primario o de ventana no son permanentes. Cuando una aplicación libera estos contextos de dispositivo, las selecciones actuales, como el modo de asignación y la región de recorte, se pierden cuando se devuelve el contexto a la memoria caché. Los cambios en un contexto de dispositivo privado o de clase se conservan indefinidamente. Para restaurarlos a sus valores predeterminados originales, una aplicación debe establecer explícitamente cada atributo.

 

 



