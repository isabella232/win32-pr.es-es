---
description: Representa una matriz de 3x3 que, a su vez, representa una transformación afín.
ms.assetid: 79abff2e-d1d3-4a32-9ac2-f46c1b21f742
title: Clase InkTransform (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InkTransform
api_type:
- COM
api_location:
- InkObj.dll
- InkObj.dll.dll
ms.openlocfilehash: 61641f0fed8ec98321e155f82ff9a35150e7fdcd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105717159"
---
# <a name="inktransform-class"></a>Clase InkTransform

Representa una matriz de 3x3 que, a su vez, representa una transformación afín.

**InkTransform** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La clase **InkTransform** tiene estos métodos.



| Método                                                  | Descripción                                                                                                                 |
|:--------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------|
| [**GetTransform**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-gettransform)       | Recupera el **InkTransform** como 6 flotantes.<br/>                                                                      |
| [**Mostrar**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-reflect)                 | Refleja la transformación en las direcciones horizontal o vertical.<br/>                                          |
| [**Reset**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-reset)                     | Restablece el estado original de la transformación.<br/>                                                                      |
| [**Girar**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-rotate)                   | Gira la transformación por un ángulo medido en grados y, opcionalmente, especifica un punto central para la rotación.<br/> |
| [**ScaleTransform**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-scaletransform) | Escala la transformación por factores X e y.<br/>                                                                         |
| [**SetTransform**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-settransform)       | Modifica **InkTransform** con 6 flotantes.<br/>                                                                    |
| [**Sesgo**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-shear)                     | Aplica un recorte con los factores horizontales y verticales especificados.<br/>                                              |
| [**Traducir**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-translate)             | Mueve la transformación por los componentes horizontal y vertical especificados.<br/>                                         |



 

### <a name="properties"></a>Propiedades

La clase **InkTransform** tiene estas propiedades.



| Propiedad                                     | Tipo de acceso           | Descripción                                                                                          |
|:---------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------|
| [**Data**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-get_data)<br/> | Lectura/escritura<br/> | Obtiene o establece la versión de automatización del struct XFORM de WIN32.<br/>                            |
| [**eDx**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-get_edx)<br/>   | Lectura/escritura<br/> | Obtiene o establece el número real que especifica el elemento de la tercera fila, primera columna.<br/>   |
| [**eDy**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-get_edy)<br/>   | Lectura/escritura<br/> | Obtiene o establece el número real que especifica el elemento de la tercera fila, segunda columna.<br/>  |
| [**eM11**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-get_em11)<br/> | Lectura/escritura<br/> | Obtiene o establece el número real que especifica el elemento de la primera fila, la primera columna.<br/>   |
| [**eM12**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-get_em12)<br/> | Lectura/escritura<br/> | Obtiene o establece el número real que especifica el elemento de la primera fila, segunda columna.<br/>  |
| [**eM21**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-get_em21)<br/> | Lectura/escritura<br/> | Obtiene o establece el número real que especifica el elemento de la segunda fila, la primera columna.<br/>  |
| [**eM22**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-get_em22)<br/> | Lectura/escritura<br/> | Obtiene o establece el número real que especifica el elemento de la segunda fila, segunda columna.<br/> |



 

## <a name="remarks"></a>Observaciones

Se puede crear una instancia de este objeto llamando al método [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) en C++.

El objeto solo almacena seis de los nueve números en una matriz de 3x3 porque todas las matrices de 3x3 que representan transformaciones afines tienen la misma tercera columna (0, 0, 1). A su vez, este objeto se usa para describir operaciones de transformación, como mover, distorsionar, escalar o rotar en un objeto [**InkRenderer**](inkrenderer-class.md) , un objeto [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) o una colección [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) .

> [!Note]  
> El objeto **InkTransform** se correlaciona con la estructura [**XForm**](/windows/win32/api/wingdi/ns-wingdi-xform) .

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]<br/>                                                       |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                           |
| Encabezado<br/>                   | <dl> <dt>Msinkaut. h (también requiere Msinkaut \_ i. c)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



 

