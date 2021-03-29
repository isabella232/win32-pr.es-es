---
title: Enumerar grupos locales
description: En los servidores miembro y equipos que ejecutan Windows 2000 Professional, puede enumerar todos los grupos locales.
ms.assetid: edbabbe5-13e1-42f6-8e73-f8e18ba4866b
ms.tgt_platform: multiple
keywords:
- Enumerar los grupos locales AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6e106fc2517cfedd8fb5fa40e4b99798ee32de8
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "103789567"
---
# <a name="enumerating-local-groups"></a>Enumerar grupos locales

En los servidores miembro y equipos que ejecutan Windows 2000 Professional, puede enumerar todos los grupos locales.

Solo se pueden crear grupos locales en servidores miembro y Windows 2000 Professional. Sin embargo, esos grupos locales pueden contener:

-   Grupos universales y globales del bosque que contiene el dominio al que pertenece el equipo.
-   Grupos locales de dominio del dominio del equipo.
-   Usuarios de cualquier dominio del bosque.

**Para enumerar los grupos locales en un servidor miembro o un equipo que ejecuta Windows 2000 Professional**

1.  Enlazar al equipo mediante las siguientes reglas:
    1.  Use una cuenta con derechos suficientes para tener acceso a ese equipo.
    2.  Use el siguiente formato de cadena de enlace con el proveedor de WinNT, el nombre del equipo y un parámetro adicional para indicar a ADSI que está enlazando a un equipo: "WinNT:// <computer name> <computer> ".

        El parámetro "el <computer name> " es el nombre del grupo de equipos al que se va a obtener acceso. Este parámetro indica a ADSI que se enlaza a un equipo y permite que el analizador del proveedor de WinNT omita algunas consultas de resolución de ambigüedades para determinar el tipo de objeto al que se está enlazando.

    3.  Enlazar a la interfaz [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) .

2.  Establezca un filtro que contenga "groups" mediante la propiedad [**IADsContainer. Filter**](/windows/desktop/api/iads/nn-iads-iadscontainer) . Esto le permite enumerar el contenedor y recuperar solo los grupos.
3.  Enumerar los objetos de grupo mediante el método [**IADsContainer:: get \_ \_ NewEnum**](/windows/desktop/api/iads/nf-iads-iadscontainer-get__newenum) .
4.  Para cada objeto de grupo, use la interfaz [**IADsGroup**](/windows/desktop/api/iads/nn-iads-iadsgroup) para leer el nombre y los miembros del grupo.

 

 