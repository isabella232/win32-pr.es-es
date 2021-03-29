---
title: Eliminar una partición de directorio de aplicaciones
description: Una partición de directorio de aplicaciones se elimina eliminando el objeto crossRef que representa la partición del directorio de aplicaciones.
ms.assetid: bc7986c1-5a11-440c-924e-dc525b5cb78f
ms.tgt_platform: multiple
keywords:
- Eliminar una partición de directorio de aplicaciones AD
- Particiones de directorio de aplicaciones, eliminar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd52ef99323ee7463a4733210314e02d911f0d66
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "103789580"
---
# <a name="deleting-an-application-directory-partition"></a>Eliminar una partición de directorio de aplicaciones

Una partición de directorio de aplicaciones se elimina eliminando el objeto [**crossRef**](/windows/desktop/ADSchema/c-crossref) que representa la partición del directorio de aplicaciones. Cuando la eliminación del objeto **crossRef** se replica en un controlador de dominio que tiene una réplica de la partición de directorio de aplicaciones, el KCC eliminará la réplica local de la partición de directorio de aplicaciones. Esto hace que se eliminen todas las réplicas de la partición de directorio de aplicaciones.

Cuando se elimina el objeto [**crossRef**](/windows/desktop/ADSchema/c-crossref) , el servidor de Active Directory eliminará el objeto [**domainDNS**](/windows/desktop/ADSchema/c-domaindns) que se creó cuando se creó la partición del directorio de aplicaciones, así como la eliminación de todos los objetos de la partición del directorio de aplicaciones. Ninguno de los objetos de la partición de directorio de aplicaciones se extingue cuando se eliminan.

Cuando se elimina una partición de directorio de aplicaciones, es muy difícil restaurarla. Para restaurar una partición de directorio de aplicaciones, es necesario restaurar una copia de seguridad que tenga una réplica de la partición de directorio de aplicaciones, buscar el objeto [**crossRef**](/windows/desktop/ADSchema/c-crossref) que representa la partición del directorio de aplicaciones y restaurar de forma autoritativa el objeto **crossRef** .

**Para eliminar una partición del directorio de aplicaciones y sus réplicas, realice los pasos siguientes:**

1.  Busque en el contenedor de particiones un objeto [**crossRef**](/windows/desktop/ADSchema/c-crossref) que tenga un valor de atributo [**NCName**](/windows/desktop/ADSchema/a-ncname) que sea igual al nombre distintivo de la partición de directorio de aplicaciones.
2.  Elimine el objeto [**crossRef**](/windows/desktop/ADSchema/c-crossref) .

Para obtener más información, consulte el [código de ejemplo para eliminar una partición de directorio de aplicaciones](example-code-for-deleting-an-application-directory-partition.md).

 

 