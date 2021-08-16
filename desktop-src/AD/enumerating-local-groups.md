---
title: Enumeración de grupos locales
description: En servidores miembros y equipos que se ejecutan Windows 2000 Professional, puede enumerar todos los grupos locales.
ms.assetid: edbabbe5-13e1-42f6-8e73-f8e18ba4866b
ms.tgt_platform: multiple
keywords:
- Enumeración de grupos locales de AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f1584cf8650b3fa341e7a314e0b6f94120b28c50226f16230c53206d6e14b80
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118191335"
---
# <a name="enumerating-local-groups"></a>Enumeración de grupos locales

En servidores miembros y equipos que se ejecutan Windows 2000 Professional, puede enumerar todos los grupos locales.

Solo se pueden crear grupos locales en servidores miembros y Windows 2000 Professional. Sin embargo, esos grupos locales pueden contener:

-   Grupos universales y globales del bosque que contiene el dominio al que es miembro el equipo.
-   Grupos locales de dominio del dominio de ese equipo.
-   Usuarios de cualquier dominio del bosque.

**Para enumerar los grupos locales en un servidor miembro o equipo que ejecuta Windows 2000 Professional**

1.  Enlace al equipo mediante las siguientes reglas:
    1.  Use una cuenta con derechos suficientes para acceder a ese equipo.
    2.  Use el siguiente formato de cadena de enlace con el proveedor winNT, el nombre del equipo y un parámetro adicional para indicar a ADSI que está enlazando a un equipo: "WinNT:// <computer name> , <computer> ".

        El parámetro "" es el nombre del grupo de equipos al que <computer name> se va a acceder. Este parámetro indica a ADSI que está enlazando a un equipo y permite que el analizador del proveedor winNT omita algunas consultas de resolución de ambigüedad para determinar a qué tipo de objeto está enlazando.

    3.  Enlace a la [**interfaz IADsContainer.**](/windows/desktop/api/iads/nn-iads-iadscontainer)

2.  Establezca un filtro que contenga "grupos" mediante la [**propiedad IADsContainer.Filter.**](/windows/desktop/api/iads/nn-iads-iadscontainer) Esto le permite enumerar el contenedor y recuperar solo los grupos.
3.  Enumere los objetos de grupo mediante [**el método IADsContainer::get \_ \_ NewEnum.**](/windows/desktop/api/iads/nf-iads-iadscontainer-get__newenum)
4.  Para cada objeto de grupo, use la [**interfaz IADsGroup**](/windows/desktop/api/iads/nn-iads-iadsgroup) para leer el nombre y los miembros del grupo.

 

 