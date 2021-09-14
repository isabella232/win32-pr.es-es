---
description: Una ACL de objetos puede contener LASA heredadas de su contenedor primario.
ms.assetid: a9e5ad4d-61c6-43ed-a162-460683bcdb16
title: Herencia de ACE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d6462ed9523c94090924981db252b938f2056cf
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073738"
---
# <a name="ace-inheritance"></a>Herencia de ACE

La ACL de un objeto puede contener LASA heredadas de su contenedor primario. Por ejemplo, una subclave del Registro puede heredar las ACE de la clave encima de ella en la jerarquía del Registro. Del mismo modo, un archivo de un sistema de archivos NTFS puede heredar las ACE del directorio que lo contiene.

La [**estructura \_ ACE HEADER**](/windows/desktop/api/Winnt/ns-winnt-ace_header) de una ACE contiene un conjunto de marcas de herencia que controlan la herencia ace y el efecto de una ACE en el objeto al que está adjunta. El sistema interpreta las marcas de herencia y otra información de herencia según las [reglas de herencia ACE](ace-inheritance-rules.md).

Estas reglas se han mejorado con las siguientes características:

-   Compatibilidad con [la propagación automática de ACE heredables.](automatic-propagation-of-inheritable-aces.md)
-   Marca que diferencia entre las ACE heredadas y las ACE que se aplicaron directamente a un objeto.
-   ACE específicas del objeto que le permiten especificar el tipo de objeto secundario que puede heredar la ACE.
-   La capacidad de evitar que una DACL o SACL herede las ACE estableciendo los bits DACL PROTECTED o SE SACL PROTECTED de SE en los bits de control del descriptor de seguridad, excepto en el caso de LA ACE del atributo DE ATRIBUTO DE RECURSO DEL SISTEMA y la ACE de id. de directiva con ámbito del \_ \_ \_ \_ [](/windows/desktop/SecGloss/s-gly) \_ \_ \_ \_ \_ \_ \_ sistema.

 

 
