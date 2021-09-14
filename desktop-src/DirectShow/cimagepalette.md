---
description: La clase CImagePalette administra paletas para representadores de vídeo. Se puede usar para crear una paleta lógica a partir de un formato de vídeo. Esta clase está pensada para usarse con las clases CBaseWindow y CDrawImage, por lo que es ligeramente especializada.
ms.assetid: dcbe5049-0e8c-4221-825a-0fd8e6efd2a5
title: CImagePalette (clase)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127273092"
---
# <a name="cimagepalette-class"></a>CImagePalette (clase)

La `CImagePalette` clase administra paletas para representadores de vídeo. Se puede usar para crear una paleta lógica a partir de un formato de vídeo. Esta clase está pensada para usarse con las clases [**CBaseWindow**](cbasewindow.md) y [**CDrawImage,**](cdrawimage.md) por lo que es ligeramente especializada.



| Variables de miembro protegido                                       | Descripción                                                                                    |
|------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [**m \_ hPalette**](cimagepalette-m-hpalette.md)                  | Controle la paleta lógica que administra este objeto.                                        |
| [**m \_ pBaseWindow**](cimagepalette-m-pbasewindow.md)            | Puntero al **objeto CBaseWindow** que administra la ventana.                                 |
| [**m \_ pDrawImage**](cimagepalette-m-pdrawimage.md)              | Puntero al objeto **CDrawImage** que dibuja la imagen de vídeo.                               |
| [**m \_ pFilter**](cimagepalette-m-pfilter.md)                    | Puntero al filtro propietario.                                                                  |
| Métodos públicos                                                   | Descripción                                                                                    |
| [**CImagePalette**](cimagepalette-cimagepalette.md)             | Método constructor.                                                                            |
| [**CopyPalette**](cimagepalette-copypalette.md)                 | Copia la paleta de cualquier **estructura VIDEOINFO** en cualquier estructura **VIDEOINFO desenlaizada.** |
| [**MakeIdentityPalette**](cimagepalette-makeidentitypalette.md) | Intenta crear una paleta que se asigna directamente a la paleta seleccionada en el dispositivo de visualización.   |
| [**MakePalette**](cimagepalette-makepalette.md)                 | Crea una paleta lógica a partir de la tabla de colores en formato de vídeo.                              |
| [**PreparePalette**](cimagepalette-preparepalette.md)           | Configura una paleta, en función de un tipo de medio del filtro propietario.                               |
| [**RemovePalette**](cimagepalette-removepalette.md)             | Elimina la paleta lógica existente.                                                          |



 

 

 



