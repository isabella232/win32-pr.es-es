---
title: DISPIDS estándar
description: Se han definido varios problemas estándar para la especificación de controles.
ms.assetid: f938b64f-5d45-40e7-ad02-665ce9c86a70
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 657a7cd12ac92504bb5d63dcd486b6a45da47310
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127466613"
---
# <a name="standard-dispids"></a>DISPIDS estándar

Se han definido varios problemas estándar para la especificación de controles.

## <a name="dispid_mousepointer"></a>DISPID \_ MOUSEPOINTER

Propiedad de tipo integer.

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
| 7<br/>  | Tamaño N S (flecha doble que apunta hacia el norte y el sur)<br/>                |
| 8<br/>  | Tamaño NW, SE<br/>                                                     |
| 9<br/>  | Tamaño E W (flecha doble que apunta hacia el este y el oeste)<br/>                  |
| 10<br/> | Flecha arriba<br/>                                                        |
| 11<br/> | Reloj de reloj de reloj (espera)<br/>                                                |
| 12<br/> | Sin colocar<br/>                                                         |
| 13<br/> | Flecha y reloj de reloj<br/>                                             |
| 14<br/> | Flecha y signo de interrogación<br/>                                         |
| 15<br/> | Tamaño de todo<br/>                                                        |
| 99<br/> | Icono personalizado especificado por la propiedad MouseIcon<br/>                 |



 

## <a name="dispid_mouseicon"></a>ICONO DEL \_ MOUSE DISPID

Propiedad de la imagen de tipo.

``` syntax
#define DISPID_MOUSEICON               -522
```

## <a name="dispid_picture"></a>IMAGEN \_ DESACONSÍ

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

Se usa para permitir que el control obtenga el HPAL del contenedor. Si el contenedor proporciona una paleta de ambiente, esa es la única paleta que se puede realizar en primer plano. Los controles que desean obtener sus propias paletas deben hacerlo en segundo plano. Si el contenedor no proporciona ninguna paleta ambiental, el control activo puede realizar su paleta en primer plano. El control de paletas se describe más detalladamente en Comportamiento de la paleta para los controles OLE, que se encuentra en el SDK ActiveX.

``` syntax
#define DISPID_AMBIENT_PALETTE         -726
```

 

 





