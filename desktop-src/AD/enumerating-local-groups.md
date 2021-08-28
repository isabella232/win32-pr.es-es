---
title: Enumerar grupos locales
description: En servidores miembros y equipos que se ejecutan Windows 2000 Professional, puede enumerar todos los grupos locales.
ms.assetid: edbabbe5-13e1-42f6-8e73-f8e18ba4866b
ms.tgt_platform: multiple
keywords:
- Enumeración de grupos locales de AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6dcecf0f16cb0679e190197f0677cb9b23a96195
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122881422"
---
# <a name="enumerating-local-groups"></a>Enumerar grupos locales

En servidores miembros y equipos que se ejecutan Windows 2000 Professional, puede enumerar todos los grupos locales.

Solo se pueden crear grupos locales en servidores miembros y Windows 2000 Professional. Sin embargo, esos grupos locales pueden contener:

-   Grupos universales y globales del bosque que contiene el dominio al que es miembro el equipo.
-   Grupos locales de dominio del dominio de ese equipo.
-   Usuarios de cualquier dominio del bosque.

**Para enumerar los grupos locales en un servidor miembro o equipo que ejecuta Windows 2000 Professional**

1.  Enlace al equipo mediante las siguientes reglas:
    1.  Use una cuenta con derechos suficientes para acceder a ese equipo.
    2.  Use el siguiente formato de cadena de enlace mediante el proveedor WinNT, el nombre del equipo y un parámetro adicional para indicar a ADSI que está enlazando a un equipo: "WinNT:// <computer name> , &lt; &gt; equipo".

        El <computer name> parámetro "" es el nombre del grupo de equipos al que se va a acceder. Este parámetro indica a ADSI que está enlazando a un equipo y permite que el analizador del proveedor winNT omita algunas consultas de resolución de ambigüedad para determinar a qué tipo de objeto está enlazando.

    3.  Enlace a la [**interfaz IADsContainer.**](/windows/desktop/api/iads/nn-iads-iadscontainer)

2.  Establezca un filtro que contenga "grupos" mediante [**la propiedad IADsContainer.Filter.**](/windows/desktop/api/iads/nn-iads-iadscontainer) Esto le permite enumerar el contenedor y recuperar solo los grupos.
3.  Enumere los objetos de grupo mediante [**el método IADsContainer::get \_ \_ NewEnum.**](/windows/desktop/api/iads/nf-iads-iadscontainer-get__newenum)
4.  Para cada objeto de grupo, use la [**interfaz IADsGroup**](/windows/desktop/api/iads/nn-iads-iadsgroup) para leer el nombre y los miembros del grupo.

 

 
