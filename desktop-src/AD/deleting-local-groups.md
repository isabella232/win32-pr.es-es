---
title: Eliminar grupos locales
description: En este tema se muestra cómo eliminar un grupo local de un servidor miembro o un equipo que ejecuta en Windows 2000 Professional.
ms.assetid: 030da25a-a606-4521-a243-d902c772fd00
ms.tgt_platform: multiple
keywords:
- Eliminar grupos locales AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14b55f90a8e6ac5cb77bf878d5ac680a6da91f73
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "104487463"
---
# <a name="deleting-local-groups"></a>Eliminar grupos locales

En este tema se muestra cómo eliminar un grupo local de un servidor miembro o un equipo que ejecuta en Windows 2000 Professional.

**Para eliminar un grupo local**

1.  Enlazar al equipo mediante las siguientes reglas:
    1.  Use una cuenta con derechos suficientes para tener acceso a ese equipo.
    2.  Use el siguiente formato de cadena de enlace con el proveedor de WinNT, el nombre del equipo y un parámetro adicional para indicar a ADSI que está enlazando a un equipo: "WinNT:// <computer name> <computer> ". El &lt; parámetro "nombre &gt; de equipo" es el nombre del grupo de equipos al que se va a obtener acceso. Este parámetro indica a ADSI que se enlaza a un equipo y permite que el analizador del proveedor de WinNT omita algunas consultas de resolución de ambigüedades para determinar el tipo de objeto al que se está enlazando.
    3.  Enlazar a la interfaz [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) .
2.  Especifique "Group" como la clase mediante [**IADsContainer. Delete**](/windows/desktop/api/iads/nf-iads-iadscontainer-delete)para eliminar el grupo.

    No es necesario llamar a [**IADs. SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) para confirmar el cambio en el contenedor. La llamada [**IADsContainer. Delete**](/windows/desktop/api/iads/nf-iads-iadscontainer-delete) confirma la eliminación del grupo directamente en el directorio.

 

 