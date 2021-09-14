---
title: Constantes de navegación (Oleacc.h)
description: En este tema se describen los valores constantes, definidos en oleacc.h, que indican la dirección espacial (arriba, abajo, izquierda y derecha) o la dirección lógica (primer elemento secundario, último, siguiente y anterior) observada cuando los clientes usan IAccessible accNavigate para navegar de un elemento de la interfaz de usuario a otro dentro del mismo contenedor.
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127070675"
---
# <a name="navigation-constants"></a>Constantes de navegación

En este tema se describen los valores constantes, definidos  en oleacc.h, que indican la dirección espacial (arriba, abajo, izquierda y derecha) o lógica *(primera* secundaria, última, siguiente y anterior) observada cuando los clientes usan [**IAccessible::accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) para navegar de un elemento de interfaz de usuario a otro dentro del mismo contenedor. Para obtener más información, vea [Propiedades y métodos de navegación de objetos.](object-navigation-properties-and-methods.md)

Las Microsoft Active Accessibility de navegación son las siguientes:



| Constante                                                                                                                                                                  | Descripción                                                                                                                                           |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="NAVDIR_DOWN"></span><span id="navdir_down"></span><dl> <dt>**NAVDIR \_ DOWN**</dt> </dl>                   | Vaya al objeto relacionado que se encuentra debajo del objeto de inicio.<br/>                                                                  |
| <span id="NAVDIR_FIRSTCHILD"></span><span id="navdir_firstchild"></span><dl> <dt>**NAVDIR \_ FIRSTCHILD**</dt> </dl> | Vaya al primer elemento secundario de este objeto. Cuando se usa esta marca, el **miembro lVal** del *parámetro varStart* debe ser CHILDID \_ SELF.<br/> |
| <span id="NAVDIR_LASTCHILD"></span><span id="navdir_lastchild"></span><dl> <dt>**NAVDIR \_ LASTCHILD**</dt> </dl>    | Vaya al último elemento secundario de este objeto. Cuando se usa esta marca, el **miembro lVal** del *parámetro varStart* debe ser CHILDID \_ SELF.<br/>    |
| <span id="NAVDIR_LEFT"></span><span id="navdir_left"></span><dl> <dt>**NAVDIR \_ LEFT**</dt> </dl>                   | Vaya al objeto relacionado situado a la izquierda del objeto de inicio.<br/>                                                                 |
| <span id="NAVDIR_NEXT"></span><span id="navdir_next"></span><dl> <dt>**NAVDIR \_ NEXT**</dt> </dl>                   | Vaya al siguiente objeto lógico; por lo general, es un elemento relacionado del objeto de inicio.<br/>                                                    |
| <span id="NAVDIR_PREVIOUS"></span><span id="navdir_previous"></span><dl> <dt>**NAVDIR \_ PREVIOUS**</dt> </dl>       | Vaya al objeto lógico anterior; por lo general, es un elemento relacionado del objeto de inicio.<br/>                                                |
| <span id="NAVDIR_RIGHT"></span><span id="navdir_right"></span><dl> <dt>**NAVDIR \_ RIGHT**</dt> </dl>                | Vaya al objeto relacionado que se encuentra a la derecha del objeto de inicio.<br/>                                                        |
| <span id="NAVDIR_UP"></span><span id="navdir_up"></span><dl> <dt>**NAVDIR \_ UP**</dt> </dl>                         | Vaya al objeto relacionado que se encuentra encima del objeto de inicio.<br/>                                                                  |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Oleacc.h</dt> </dl> |



 

 





