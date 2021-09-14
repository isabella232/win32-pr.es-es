---
description: Las siguientes funciones se usan con DDE de red.
ms.assetid: 5fd61759-1792-4db0-9ad4-adf112294b9c
title: Funciones DDE de red
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16e5ae6a38ec6324cf33b4f9c4ffc1af44473699
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359155"
---
# <a name="network-dde-functions"></a>Funciones DDE de red

\[Ya no se admite DDE de red. Nddeapi.dll está presente en Windows Vista, pero todas las llamadas de función devuelven NDDE \_ NOT \_ IMPLEMENTED.\]

Las siguientes funciones se usan con DDE de red.



| Función                                                   | Descripción                                                                                                           |
|------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [**NDdeGetErrorString**](nddegeterrorstring.md)           | Convierte un código de error devuelto por una función DDE de red en una cadena de error que explica el código de error devuelto. |
| [**NDdeGetShareSecurity**](nddegetsharesecurity.md)       | Recupera el descriptor de seguridad asociado al recurso compartido de DDE.                                                      |
| [**NDdeGetTrustedShare**](nddegettrustedshare.md)         | Recupera las opciones asociadas a un recurso compartido de DDE que se encuentra en la lista de recursos compartidos de confianza del usuario del servidor.                |
| [**NDdeIsValidAppTopicList**](nddeisvalidapptopiclist.md) | Determina si una aplicación y una cadena de tema ("*AppName* \| *TopicName*") usa la sintaxis adecuada.                 |
| [**NDdeIsValidShareName**](nddeisvalidsharename.md)       | Determina si un nombre de recurso compartido usa la sintaxis adecuada.                                                               |
| [**NDdeSetShareSecurity**](nddesetsharesecurity.md)       | Establece el descriptor de seguridad asociado al recurso compartido de DDE.                                                           |
| [**NDdeSetTrustedShare**](nddesettrustedshare.md)         | Concede el estado de confianza del recurso compartido de DDE especificado en el contexto del usuario actual.                                      |
| [**NDdeShareAdd**](nddeshareadd.md)                       | Crea y agrega un nuevo recurso compartido de DDE al administrador de bases de datos de recursos compartidos de DDE (DSDM).                                            |
| [**NDdeShareDel**](nddesharedel.md)                       | Elimina un recurso compartido DDE del DSDM.                                                                                    |
| [**NDdeShareEnum**](nddeshareenum.md)                     | Recupera la lista de recursos compartidos DDE disponibles.                                                                           |
| [**NDdeShareGetInfo**](nddesharegetinfo.md)               | Recupera la información del recurso compartido de DDE.                                                                                      |
| [**NDdeShareSetInfo**](nddesharesetinfo.md)               | Establece la información del recurso compartido de DDE.                                                                                           |
| [**NDdeTrustedShareEnum**](nddetrustedshareenum.md)       | Recupera los nombres de todos los recursos compartidos DDE de red de confianza en el contexto del proceso de llamada.                 |



 

 

 



