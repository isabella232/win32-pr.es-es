---
title: Funciones de seguridad
description: Las funciones de seguridad de administración de red obtienen y establecen descriptores de seguridad para raíces independientes y basadas en dominio DFS.
ms.assetid: 90860842-0f4d-49ad-b835-50305328a050
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d31611aa650bb55ecdc29af468e0ef784b670555b247d536d27b397de356f4ec
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119677805"
---
# <a name="security-functions"></a>Funciones de seguridad

Las funciones de seguridad de administración de red obtienen y establecen descriptores de seguridad para raíces independientes y basadas en dominio DFS.

Las funciones de seguridad DFS se enumeran a continuación.

| Función                                                               | Descripción                                                                                                          |
|------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [**NetDfsGetSecurity**](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetsecurity)                         | Obtiene el descriptor de seguridad para el objeto raíz de la raíz DFS especificada.                                       |
| [**NetDfsSetSecurity**](/windows/desktop/api/lmdfs/nf-lmdfs-netdfssetsecurity)                         | Busca el objeto raíz para la raíz DFS especificada y establece en él el descriptor de seguridad proporcionado.                  |
| [**NetDfsGetStdContainerSecurity**](/windows/desktop/api/lmdfs/nf-lmdfs-netdfssetftcontainersecurity) | Obtiene el descriptor de seguridad para el objeto contenedor de la raíz independiente DFS especificada.                      |
| [**NetDfsSetStdContainerSecurity**](/windows/desktop/api/lmdfs/nf-lmdfs-netdfssetstdcontainersecurity) | Busca el objeto contenedor para la raíz independiente de DFS especificada y establece en él el descriptor de seguridad proporcionado. |
| [**NetDfsGetFtContainerSecurity**](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetftcontainersecurity)   | Obtiene el descriptor de seguridad para el objeto contenedor de la raíz de dominio DFS especificada.                           |
| [**NetDfsSetFtContainerSecurity**](/windows/desktop/api/lmdfs/nf-lmdfs-netdfssetftcontainersecurity)   | Busca el objeto contenedor para la raíz de dominio DFS especificada y establece en él el descriptor de seguridad proporcionado.      |
