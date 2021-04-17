---
title: Constantes de navegación (oleacc. h)
description: En este tema se describen los valores constantes, definidos en oleacc. h, que indican la dirección espacial (arriba, abajo, izquierda y derecha) o lógica (primer elemento secundario, último, siguiente y anterior) observada cuando los clientes usan IAccessible accNavigate para desplazarse de un elemento de la interfaz de usuario a otro dentro del mismo contenedor.
ms.assetid: 5859a7a3-bcd3-443e-8ff0-4952f4639517
topic_type:
- apiref
api_name:
- NAVDIR_DOWN
- NAVDIR_FIRSTCHILD
- NAVDIR_LASTCHILD
- NAVDIR_LEFT
- NAVDIR_NEXT
- NAVDIR_PREVIOUS
- NAVDIR_RIGHT
- NAVDIR_UP
api_location:
- oleacc.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8de5f4eaa3fc7fb24583e49bdd14acb9633b2bd4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660497"
---
# <a name="navigation-constants"></a>Constantes de navegación

En este tema se describen los valores constantes, definidos en oleacc. h, que indican la dirección *espacial* (arriba, abajo, izquierda y derecha) o *lógica* (primera parte secundaria, última, siguiente y anterior) observada cuando los clientes usan [**IAccessible:: accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) para desplazarse de un elemento de la interfaz de usuario a otro dentro del mismo contenedor. Para obtener más información, vea [métodos y propiedades de navegación de objetos](object-navigation-properties-and-methods.md).

Las constantes de navegación de Microsoft Active Accessibility son las siguientes:



| Constante                                                                                                                                                                  | Descripción                                                                                                                                           |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="NAVDIR_DOWN"></span><span id="navdir_down"></span><dl> <dt>**NAVDIR \_ abajo**</dt> </dl>                   | Navegue hasta el objeto relacionado que se encuentra debajo del objeto inicial.<br/>                                                                  |
| <span id="NAVDIR_FIRSTCHILD"></span><span id="navdir_firstchild"></span><dl> <dt>**NAVDIR \_ FIRSTCHILD**</dt> </dl> | Navegue hasta el primer elemento secundario de este objeto. Cuando se usa esta marca, el miembro **lVal** del parámetro *VARSTART* debe ser CHILDID \_ Self.<br/> |
| <span id="NAVDIR_LASTCHILD"></span><span id="navdir_lastchild"></span><dl> <dt>**NAVDIR \_ LASTCHILD**</dt> </dl>    | Navegue hasta el último elemento secundario de este objeto. Cuando se usa esta marca, el miembro **lVal** del parámetro *VARSTART* debe ser CHILDID \_ Self.<br/>    |
| <span id="NAVDIR_LEFT"></span><span id="navdir_left"></span><dl> <dt>**NAVDIR a la \_ izquierda**</dt> </dl>                   | Navegue hasta el objeto relacionado situado a la izquierda del objeto inicial.<br/>                                                                 |
| <span id="NAVDIR_NEXT"></span><span id="navdir_next"></span><dl> <dt>**NAVDIR \_ siguiente**</dt> </dl>                   | Navegue hasta el siguiente objeto lógico; por lo general, es un elemento relacionado del objeto inicial.<br/>                                                    |
| <span id="NAVDIR_PREVIOUS"></span><span id="navdir_previous"></span><dl> <dt>**NAVDIR \_ anterior**</dt> </dl>       | Navegue hasta el objeto lógico anterior; por lo general, es un elemento relacionado del objeto inicial.<br/>                                                |
| <span id="NAVDIR_RIGHT"></span><span id="navdir_right"></span><dl> <dt>**NAVDIR \_ derecha**</dt> </dl>                | Navegue hasta el objeto relacionado que se encuentra a la derecha del objeto de inicio.<br/>                                                        |
| <span id="NAVDIR_UP"></span><span id="navdir_up"></span><dl> <dt>**NAVDIR \_**</dt> </dl>                         | Navegue hasta el objeto relacionado que se encuentra encima del objeto inicial.<br/>                                                                  |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Oleacc. h</dt> </dl> |



 

 





