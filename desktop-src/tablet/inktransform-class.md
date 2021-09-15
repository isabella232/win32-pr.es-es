---
description: Representa una matriz 3x3 que, a su vez, representa una transformación afín.
ms.assetid: 79abff2e-d1d3-4a32-9ac2-f46c1b21f742
title: Clase InkTransform (Mstransformut.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127466775"
---
# <a name="inktransform-class"></a>InkTransform (clase)

Representa una matriz 3x3 que, a su vez, representa una transformación afín.

**InkTransform** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La **clase InkTransform** tiene estos métodos.



| Método                                                  | Descripción                                                                                                                 |
|:--------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------|
| [**GetTransform**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-gettransform)       | Recupera **InkTransform como** 6 flotantes.<br/>                                                                      |
| [**Reflexione**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-reflect)                 | Refleja la transformación en las direcciones horizontal o vertical.<br/>                                          |
| [**Reset**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-reset)                     | Restablece la transformación a su estado original.<br/>                                                                      |
| [**Girar**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-rotate)                   | Gira la transformación mediante un ángulo medido en grados y, opcionalmente, especifica un punto central para la rotación.<br/> |
| [**ScaleTransform**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-scaletransform) | Escala la transformación por factores X e Y.<br/>                                                                         |
| [**SetTransform**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-settransform)       | Modifica **InkTransform** con 6 flotantes.<br/>                                                                    |
| [**Esquileo**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-shear)                     | Aplica una cizalla con los factores horizontal y vertical especificados.<br/>                                              |
| [**Traducir**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-translate)             | Mueve la transformación por los componentes horizontal y vertical especificados.<br/>                                         |



 

### <a name="properties"></a>Propiedades

La **clase InkTransform** tiene estas propiedades.



| Propiedad                                     | Tipo de acceso           | Descripción                                                                                          |
|:---------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------|
| [**Data**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-get_data)<br/> | Lectura y escritura<br/> | Obtiene o establece la versión de Automation de la estructura WIN32 XFORM.<br/>                            |
| [**Edx**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-get_edx)<br/>   | Lectura y escritura<br/> | Obtiene o establece el número real que especifica el elemento de la tercera fila, la primera columna.<br/>   |
| [**Edy**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-get_edy)<br/>   | Lectura y escritura<br/> | Obtiene o establece el número real que especifica el elemento de la tercera fila, segunda columna.<br/>  |
| [**eM11**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-get_em11)<br/> | Lectura y escritura<br/> | Obtiene o establece el número real que especifica el elemento de la primera fila, la primera columna.<br/>   |
| [**eM12**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-get_em12)<br/> | Lectura y escritura<br/> | Obtiene o establece el número real que especifica el elemento de la primera fila, segunda columna.<br/>  |
| [**eM21**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-get_em21)<br/> | Lectura y escritura<br/> | Obtiene o establece el número real que especifica el elemento de la segunda fila, la primera columna.<br/>  |
| [**eM22**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-get_em22)<br/> | Lectura y escritura<br/> | Obtiene o establece el número real que especifica el elemento de la segunda fila, segunda columna.<br/> |



 

## <a name="remarks"></a>Observaciones

Se puede crear una instancia de este objeto llamando al [**método CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) en C++.

El objeto almacena solo seis de los nueve números en una matriz 3x3 porque todas las matrices de 3x3 que representan transformaciones afín tienen la misma tercera columna (0, 0, 1). A su vez, este objeto se usa para describir operaciones de transformación como mover, escalar, escalar o girar en un objeto [**InkRenderer,**](inkrenderer-class.md) un objeto [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) o una colección [InkStrokes.](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))

> [!Note]  
> El **objeto InkTransform** se correlaciona con la [**estructura XFORM.**](/windows/win32/api/wingdi/ns-wingdi-xform)

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                                                       |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                           |
| Encabezado<br/>                   | <dl> <dt>Msgniut.h (también requiere Ms ashut \_ i.c)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



 

