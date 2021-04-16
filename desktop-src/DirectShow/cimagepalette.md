---
description: La clase CImagePalette administra las paletas de representadores de vídeo. Se puede usar para crear una paleta lógica a partir de un formato de vídeo. Esta clase está pensada para usarse con las clases CBaseWindow y CDrawImage, por lo que es algo especializado.
ms.assetid: dcbe5049-0e8c-4221-825a-0fd8e6efd2a5
title: Clase CImagePalette
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImagePalette
api_type:
- COM
api_location: ''
ms.openlocfilehash: 696c51e4918815e18accbadd66c764493dc0b98e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105677061"
---
# <a name="cimagepalette-class"></a>Clase CImagePalette

La `CImagePalette` clase administra las paletas para los representadores de vídeo. Se puede usar para crear una paleta lógica a partir de un formato de vídeo. Esta clase está pensada para usarse con las clases [**CBaseWindow**](cbasewindow.md) y [**CDrawImage**](cdrawimage.md) , por lo que es algo especializado.



| Variables de miembro protegidas                                       | Descripción                                                                                    |
|------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [**m \_ hPalette**](cimagepalette-m-hpalette.md)                  | Identificador de la paleta lógica que este objeto administra.                                        |
| [**m \_ pBaseWindow**](cimagepalette-m-pbasewindow.md)            | Puntero al objeto **CBaseWindow** que administra la ventana.                                 |
| [**m \_ pDrawImage**](cimagepalette-m-pdrawimage.md)              | Puntero al objeto **CDrawImage** que dibuja la imagen de vídeo.                               |
| [**m \_ pFilter**](cimagepalette-m-pfilter.md)                    | Puntero al filtro propietario.                                                                  |
| Métodos públicos                                                   | Descripción                                                                                    |
| [**CImagePalette**](cimagepalette-cimagepalette.md)             | Método de constructor.                                                                            |
| [**CopyPalette**](cimagepalette-copypalette.md)                 | Copia la paleta de cualquier estructura de **videoinfo** en cualquier estructura de **videoinformación** de paleta. |
| [**MakeIdentityPalette**](cimagepalette-makeidentitypalette.md) | Intenta crear una paleta que se asigna directamente a la paleta seleccionada en el dispositivo de pantalla.   |
| [**MakePalette**](cimagepalette-makepalette.md)                 | Crea una paleta lógica a partir de la tabla de colores en un formato de vídeo.                              |
| [**PreparePalette**](cimagepalette-preparepalette.md)           | Configura una paleta basada en un tipo de medio del filtro propietario.                               |
| [**RemovePalette**](cimagepalette-removepalette.md)             | Elimina la paleta lógica existente.                                                          |



 

 

 



