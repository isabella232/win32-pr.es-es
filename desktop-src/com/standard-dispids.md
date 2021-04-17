---
title: DISPID estándar
description: Se ha definido un número de DISPID estándar para la especificación de los controles.
ms.assetid: f938b64f-5d45-40e7-ad02-665ce9c86a70
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 657a7cd12ac92504bb5d63dcd486b6a45da47310
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105704609"
---
# <a name="standard-dispids"></a>DISPID estándar

Se ha definido un número de DISPID estándar para la especificación de los controles.

## <a name="dispid_mousepointer"></a>desspid- \_ MOUSEPOINTER

Propiedad de tipo Integer.

``` syntax
#define DISPID_MOUSEPOINTER            -521
```

La propiedad MousePointer identifica los iconos del mouse estándar.



| Value         | Descripción                                                                |
|---------------|----------------------------------------------------------------------------|
| 0<br/>  | Predeterminada Forma determinada por el objeto.<br/>                       |
| 1<br/>  | Flecha<br/>                                                           |
| 2<br/>  | Cross (puntero de Cruz)<br/>                                      |
| 3<br/>  | I<br/>                                                          |
| 4<br/>  | Icono (cuadrado pequeño dentro de un cuadrado)<br/>                             |
| 5<br/>  | Tamaño (flecha de cuatro puntas que apunta al norte, sur, este y oeste)<br/> |
| 6<br/>  | Tamaño NE SW (doble flecha que apunta al noreste y suroeste)<br/>      |
| 7<br/>  | Tamaño N S (flecha doble que apunta al norte y al sur)<br/>                |
| 8<br/>  | Tamaño NW, SE<br/>                                                     |
| 9<br/>  | Tamaño E W (flecha doble que señala al este y oeste)<br/>                  |
| 10<br/> | Flecha arriba<br/>                                                        |
| 11<br/> | Reloj de arena (esperar)<br/>                                                |
| 12<br/> | No eliminar<br/>                                                         |
| 13<br/> | Flecha y reloj de arena<br/>                                             |
| 14<br/> | Flecha y signo de interrogación<br/>                                         |
| 15<br/> | Ajustar todo<br/>                                                        |
| 99<br/> | Icono personalizado especificado por la propiedad MouseIcon<br/>                 |



 

## <a name="dispid_mouseicon"></a>MOUSEICON de DISPID \_

Propiedad de tipo imagen.

``` syntax
#define DISPID_MOUSEICON               -522
```

## <a name="dispid_picture"></a>imagen de DISPID \_

Propiedad de tipo imagen.

``` syntax
#define DISPID_PICTURE                 -523
```

## <a name="dispid_valid"></a>DISPID \_ válido

Se utiliza para determinar si el control tiene datos válidos o no.

Propiedad de tipo BOOL.

``` syntax
#define DISPID_VALID                   -524
```

## <a name="dispid_-ambient_palette"></a>paleta ambiente de DISPID \_ \_

Se utiliza para permitir que el control obtenga el HPAL del contenedor. Si el contenedor proporciona una paleta ambiente, es la única paleta que se puede realizar en primer plano. Los controles que deseen obtener sus propias paletas deben hacerlo en segundo plano. Si no hay ninguna paleta ambiente proporcionada por el contenedor, el control activo puede obtener su paleta en primer plano. El control de paleta se describe con más detalle en el comportamiento de la paleta para los controles OLE que se encuentra en el SDK de ActiveX.

``` syntax
#define DISPID_AMBIENT_PALETTE         -726
```

 

 





