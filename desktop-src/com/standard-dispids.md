---
title: DISPIDS estándar
description: Se han definido varios problemas estándar para la especificación de controles.
ms.assetid: f938b64f-5d45-40e7-ad02-665ce9c86a70
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af35ce4e4cad884b54bb0982037721608364a0249d3be6dd566f3aac766bb1f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119129787"
---
# <a name="standard-dispids"></a>DISPIDS estándar

Se han definido varios problemas estándar para la especificación de controles.

## <a name="dispid_mousepointer"></a>DISPID \_ MOUSEPOINTER

Propiedad de tipo entero.

``` syntax
#define DISPID_MOUSEPOINTER            -521
```

La propiedad Mousepointer identifica los iconos estándar del mouse.



| Value         | Descripción                                                                |
|---------------|----------------------------------------------------------------------------|
| 0<br/>  | (Valor predeterminado) Forma determinada por el objeto .<br/>                       |
| 1<br/>  | Flecha<br/>                                                           |
| 2<br/>  | Cross (puntero de vello cruzado)<br/>                                      |
| 3<br/>  | I Beam<br/>                                                          |
| 4<br/>  | Icono (cuadrado pequeño dentro de un cuadrado)<br/>                             |
| 5<br/>  | Tamaño (flecha de cuatro puntas que apunta al norte, sur, este y oeste)<br/> |
| 6<br/>  | Tamaño NE SW (flecha doble que apunta al noreste y al suroeste)<br/>      |
| 7<br/>  | Tamaño N S (flecha doble que apunta al norte y al sur)<br/>                |
| 8<br/>  | Tamaño NW, SE<br/>                                                     |
| 9<br/>  | Tamaño E W (flecha doble que señala este y oeste)<br/>                  |
| 10<br/> | Flecha arriba<br/>                                                        |
| 11<br/> | Reloj de reloj (espera)<br/>                                                |
| 12<br/> | Sin quitar<br/>                                                         |
| 13<br/> | Flecha y reloj de reloj<br/>                                             |
| 14<br/> | Flecha y signo de interrogación<br/>                                         |
| 15<br/> | Tamaño de todo<br/>                                                        |
| 99<br/> | Icono personalizado especificado por la propiedad MouseIcon<br/>                 |



 

## <a name="dispid_mouseicon"></a>ICONO DEL \_ MOUSE DISPID

Propiedad de la imagen de tipo.

``` syntax
#define DISPID_MOUSEICON               -522
```

## <a name="dispid_picture"></a>IMAGEN \_ DESPID

Propiedad de la imagen de tipo.

``` syntax
#define DISPID_PICTURE                 -523
```

## <a name="dispid_valid"></a>DISPID \_ VÁLIDO

Se usa para determinar si el control tiene datos válidos o no.

Propiedad de tipo BOOL.

``` syntax
#define DISPID_VALID                   -524
```

## <a name="dispid_-ambient_palette"></a>PALETA \_ AMBIENTAL DISPID \_

Se usa para permitir que el control obtenga el HPAL del contenedor. Si el contenedor proporciona una paleta ambiente, esa es la única paleta que se puede realizar en primer plano. Los controles que quieran realizar sus propias paletas deben hacerlo en segundo plano. Si el contenedor no proporciona ninguna paleta ambiente, el control activo puede realizar su paleta en primer plano. El control de paletas se describe más adelante en Comportamiento de la paleta para controles OLE, que se encuentra en el SDK ActiveX.

``` syntax
#define DISPID_AMBIENT_PALETTE         -726
```

 

 





