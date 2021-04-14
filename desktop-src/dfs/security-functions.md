---
title: Funciones de seguridad
description: Las funciones de seguridad de administración de redes obtienen y establecen descriptores de seguridad para las raíces basadas en dominio DFS y independientes.
ms.assetid: 90860842-0f4d-49ad-b835-50305328a050
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95f717ff3f5701e507087fcdac164d9357f2505a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496637"
---
# <a name="security-functions"></a>Funciones de seguridad

Las funciones de seguridad de administración de redes obtienen y establecen descriptores de seguridad para las raíces basadas en dominio DFS y independientes.

A continuación se enumeran las funciones de seguridad de DFS.

| Función                                                               | Descripción                                                                                                          |
|------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [**NetDfsGetSecurity**](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetsecurity)                         | Obtiene el descriptor de seguridad para el objeto raíz de la raíz DFS especificada.                                       |
| [**NetDfsSetSecurity**](/windows/desktop/api/lmdfs/nf-lmdfs-netdfssetsecurity)                         | Busca el objeto raíz de la raíz DFS especificada y establece el descriptor de seguridad proporcionado en él.                  |
| [**NetDfsGetStdContainerSecurity**](/windows/desktop/api/lmdfs/nf-lmdfs-netdfssetftcontainersecurity) | Obtiene el descriptor de seguridad para el objeto contenedor de la raíz independiente DFS especificada.                      |
| [**NetDfsSetStdContainerSecurity**](/windows/desktop/api/lmdfs/nf-lmdfs-netdfssetstdcontainersecurity) | Busca el objeto contenedor de la raíz independiente DFS especificada y establece el descriptor de seguridad proporcionado en él. |
| [**NetDfsGetFtContainerSecurity**](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetftcontainersecurity)   | Obtiene el descriptor de seguridad para el objeto contenedor de la raíz de dominio DFS especificada.                           |
| [**NetDfsSetFtContainerSecurity**](/windows/desktop/api/lmdfs/nf-lmdfs-netdfssetftcontainersecurity)   | Busca el objeto contenedor para la raíz de dominio DFS especificada y establece el descriptor de seguridad proporcionado en él.      |
