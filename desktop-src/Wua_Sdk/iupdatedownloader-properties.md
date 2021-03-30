---
description: La interfaz IUpdateDownloader define las siguientes propiedades.
ms.assetid: b6a30356-f97d-408f-becd-a467e9f8e79f
title: Propiedades de IUpdateDownloader
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99c16aa762bcc14dc1919ef91d162752652c327e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810213"
---
# <a name="iupdatedownloader-properties"></a>Propiedades de IUpdateDownloader

La interfaz [**IUpdateDownloader**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatedownloader) define las siguientes propiedades.



| Propiedad                                                             | Descripción                                                                                                                                                                |
|----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ClientApplicationID**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatedownloader-get_clientapplicationid) | Obtiene y establece la aplicación cliente actual.                                                                                                                              |
| [**IsForced**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatedownloader-get_isforced)                       | Obtiene y establece un valor booleano que indica si el agente de Windows Update (WUA) fuerza la descarga de actualizaciones que ya están instaladas o que no se pueden instalar. |
| [**Priority**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatedownloader-get_priority)                       | Obtiene y establece el nivel de prioridad de la descarga.                                                                                                                          |
| [**Actualizaciones**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatedownloader-get_updates)                         | Obtiene y establece una interfaz que contiene una colección de solo lectura de las actualizaciones que se especifican para su descarga.                                                            |



 

 

 



