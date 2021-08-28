---
title: Eliminación de grupos locales
description: En este tema se muestra cómo eliminar un grupo local de un servidor miembro o equipo que se ejecuta en Windows 2000 Professional.
ms.assetid: 030da25a-a606-4521-a243-d902c772fd00
ms.tgt_platform: multiple
keywords:
- Eliminación de grupos locales de AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbe960804e083ecaf8ef12e412a43b7b8db4800f
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122881477"
---
# <a name="deleting-local-groups"></a>Eliminación de grupos locales

En este tema se muestra cómo eliminar un grupo local de un servidor miembro o equipo que se ejecuta en Windows 2000 Professional.

**Para eliminar un grupo local**

1.  Enlace al equipo mediante las siguientes reglas:
    1.  Use una cuenta con derechos suficientes para acceder a ese equipo.
    2.  Use el siguiente formato de cadena de enlace con el proveedor winNT, el nombre del equipo y un parámetro adicional para indicar a ADSI que está enlazando a un equipo: "WinNT:// <computer name> , &lt; &gt; equipo". El parámetro " &lt; nombre de equipo " es el nombre del grupo de equipos al que se va a &gt; acceder. Este parámetro indica a ADSI que está enlazando a un equipo y permite que el analizador del proveedor winNT omita algunas consultas de resolución de ambigüedad para determinar a qué tipo de objeto está enlazando.
    3.  Enlace a la [**interfaz IADsContainer.**](/windows/desktop/api/iads/nn-iads-iadscontainer)
2.  Especifique "group" como clase mediante [**IADsContainer.Delete**](/windows/desktop/api/iads/nf-iads-iadscontainer-delete)para eliminar el grupo.

    No es necesario llamar a [**IADs.SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) para confirmar el cambio en el contenedor. La [**llamada a IADsContainer.Delete**](/windows/desktop/api/iads/nf-iads-iadscontainer-delete) confirma la eliminación del grupo directamente en el directorio .

 

 
