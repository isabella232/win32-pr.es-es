---
description: La interfaz IUpdateDownloader define las siguientes propiedades.
ms.assetid: b6a30356-f97d-408f-becd-a467e9f8e79f
title: Propiedades de IUpdateDownloader
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf66fbdad678ef6a78d0fa049ecb59c34be2ca9d08c873e24e82c35c9d1eb1c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117738294"
---
# <a name="iupdatedownloader-properties"></a>Propiedades de IUpdateDownloader

La [**interfaz IUpdateDownloader**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatedownloader) define las siguientes propiedades.



| Propiedad                                                             | Descripción                                                                                                                                                                |
|----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ClientApplicationID**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatedownloader-get_clientapplicationid) | Obtiene y establece la aplicación cliente actual.                                                                                                                              |
| [**IsForced**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatedownloader-get_isforced)                       | Obtiene y establece un valor booleano que indica si Windows Update Agent (WUA) fuerza la descarga de actualizaciones que ya están instaladas o que no se pueden instalar. |
| [**Priority**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatedownloader-get_priority)                       | Obtiene y establece el nivel de prioridad de la descarga.                                                                                                                          |
| [**Actualizaciones**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatedownloader-get_updates)                         | Obtiene y establece una interfaz que contiene una colección de solo lectura de las actualizaciones especificadas para la descarga.                                                            |



 

 

 



