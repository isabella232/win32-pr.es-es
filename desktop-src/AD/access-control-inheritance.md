---
title: Herencia de Access Control
description: Las entradas de control de acceso (ACE) en una lista de control de acceso (ACL) de objetos pueden pertenecer a una ACL efectiva o a una ACL heredada.
ms.assetid: 2530eef5-7804-4b27-8756-d97be1cea116
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aec7514ab8cae8b07121d84e579ccb8492b67c45
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "104149154"
---
# <a name="access-control-inheritance"></a>Herencia de Access Control

Las entradas de control de acceso (ACE) en una lista de control de acceso (ACL) de objetos pueden pertenecer a una de estas dos categorías:

-   ACL efectiva: las ACE de esta categoría se aplican al objeto.
-   Heredar ACL: los objetos creados en el contenedor heredan las ACE de esta categoría.

Cada ACE de la DACL puede pertenecer a una o varias categorías. Las categorías a las que pertenece una ACE se determinan mediante las marcas de control de herencia establecidas en la ACE.

Se pueden establecer tres marcas de control de herencia en la propiedad [**AceFlags**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) de una ACE.



| Marca                                          | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|-----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_ACE de \_ herencia de ACEFLAG de ADS \_**                | Esta marca indica que la ACE forma parte de la ACL de herencia y que los objetos secundarios heredan las marcas de control de herencia de esta ACE.                                                                                                                                                                                                                                                                                                                         |
| **ACEFLAG de anuncios \_ \_ no \_ propagar la \_ ACE de herencia \_** | Esta marca indica que la ACE forma parte de la ACL de herencia, pero que no se propagan marcas de control de herencia a objetos secundarios directos (descendientes directos) y la ACE es efectiva en los objetos secundarios directos.                                                                                                                                                                                                                                          |
| **ACEFLAG de anuncios \_ \_ solo heredan \_ \_ ACE**          | Esta marca indica que la ACE no forma parte de la ACL efectiva. Si no se establece esta marca, la ACE forma parte de la ACL vigente. Esta marca es útil para establecer los permisos que heredan los subobjetos, pero que no afectan a la accesibilidad del contenedor. Por ejemplo, si una ACE está pensada para ser heredada por objetos de usuario en una unidad organizativa, es probable que no se aplique para el acceso a la propia unidad organizativa.<br/> |



 

Las marcas ACE **\_ ACEFLAG \_ no \_ Propagate \_ inherit inherit \_** y **ADS \_ ACEFLAG \_ inherit \_ Only solo \_** son significativas si está presente **\_ \_ \_ ACE ACEFLAG inherit** . Esto se debe a que la marca de la **\_ \_ \_ ACE** de herencia de ACEFLAG de ADS agrega el comportamiento de herencia a una ACE heredable, pero no define el tipo de herencia. Las marcas ACE **\_ ACEFLAG \_ no \_ Propagate \_ inherit inherit \_** y **ADS \_ ACEFLAG \_ solo heredan \_ \_** las marcas ACE definen un tipo específico de comportamiento de la herencia.

Es importante recordar que el sistema también establece las marcas siguientes en función del tipo y el estado de la ACE.



| Marca                                    | Descripción                                           |
|-----------------------------------------|-------------------------------------------------------|
| **\_ \_ ACE heredada ACEFLAG de ADS \_**        | Esta marca indica que se heredó la ACE.       |
| **\_marcas de \_ herencia válidas de ADS ACEFLAG \_ \_** | Esta marca indica que los marcadores de herencia son válidos. |



 

En la tabla siguiente se enumeran los efectos de las distintas combinaciones de marcas para la propiedad [**AceFlags**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) de una ACE.



| Marca                                                                                                                    | Efecto en el objeto que contiene la ACE                     | Efecto en los objetos secundarios directos                                                      | Efecto en objetos por debajo de los elementos secundarios directos               |
|-------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------|-------------------------------------------------------------------------------------|-------------------------------------------------------|
| No se estableció ninguna marca.                                                                                                           | ACE vigente: ACE se aplica al objeto.               | ACE no se hereda.                                                               | ACE no se hereda.                                 |
| **\_ACE de \_ herencia de ACEFLAG de ADS \_**                                                                                          | ACE vigente                                           | ACE se hereda. ACE es una ACE efectiva.<br/>                               | ACE se hereda. ACE es una ACE efectiva.<br/> |
| **Anuncios \_ de ACEFLAG \_ heredar \_ ACE** \| **ADS \_ ACEFLAG \_ inherit \_ Only \_ ACE**                                                  | No es una ACE efectiva: ACE no se aplica al objeto. | ACE se hereda. ACE es una ACE efectiva.<br/>                               | ACE se hereda. ACE es una ACE efectiva.<br/> |
| **Anuncios \_ de ACEFLAG \_ inherit \_ ACE** \| **ADS \_ ACEFLAG \_ no \_ Propagate \_ inherit \_ ACE**                                         | ACE vigente                                           | ACE se hereda pero no tiene marcadores de herencia. ACE es una ACE efectiva<br/>  | ACE no se hereda.                                 |
| **Anuncios \_ de ACEFLAG \_ inherit \_ ACE** \| **ADS \_ ACEFLAG \_ inherit \_ Only \_ ACE** \| **ad \_ ACEFLAG \_ no \_ Propagate \_ inherit \_ ACE** | No es una ACE efectiva.                                   | ACE se hereda pero no tiene marcadores de herencia. ACE es una ACE efectiva.<br/> | ACE no se hereda.                                 |



 

 

